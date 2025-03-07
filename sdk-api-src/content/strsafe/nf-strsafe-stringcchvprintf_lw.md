---
UID: NF:strsafe.StringCchVPrintf_lW
title: StringCchVPrintf_lW function (strsafe.h)
description: Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.helpviewer_keywords: ["StringCchVPrintf_l","StringCchVPrintf_l function [Menus and Other Resources]","StringCchVPrintf_lA","StringCchVPrintf_lW","menurc.stringcchvprintf_l","strsafe/StringCchVPrintf_l","strsafe/StringCchVPrintf_lA","strsafe/StringCchVPrintf_lW"]
old-location: menurc\stringcchvprintf_l.htm
tech.root: menurc
ms.assetid: 90c83405-f2c8-480b-883c-c3ce258016cd
ms.date: 12/05/2018
ms.keywords: StringCchVPrintf_l, StringCchVPrintf_l function [Menus and Other Resources], StringCchVPrintf_lA, StringCchVPrintf_lW, menurc.stringcchvprintf_l, strsafe/StringCchVPrintf_l, strsafe/StringCchVPrintf_lA, strsafe/StringCchVPrintf_lW
f1_keywords:
- strsafe/StringCchVPrintf_l
dev_langs:
- c++
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCchVPrintf_lW (Unicode) and StringCchVPrintf_lA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- StrSafe.h
api_name:
- StringCchVPrintf_l
- StringCchVPrintf_lA
- StringCchVPrintf_lW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StringCchVPrintf_lW function


## -description


Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCchVPrintf_l</b> is similar to <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a> but includes a parameter for locale information.


## -parameters




### -param pszDest [out]

The destination buffer, which receives the formatted, null-terminated string created from <i>pszFormat</i> and <i>argList</i>.


### -param cchDest [in]

The size of the destination buffer, in characters. This value must be sufficiently large to accommodate the final formatted string plus 1 to account for the terminating null character. The maximum number of characters allowed is <b>STRSAFE_MAX_CCH</b>.


### -param pszFormat [in]

The format string. This string must be null-terminated. For more information, see <a href="https://docs.microsoft.com/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions">Format Specification Syntax</a>.


### -param locale [in]

The locale object. For more information, see <b>_create_locale</b>.


### -param argList [in]

The arguments to be inserted into the <i>pszFormat</i> string.


## -returns



This function can return one of the following values. It is strongly recommended that you use the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to test the return value of this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
There was sufficient space for the result to be copied to <i>pszDest</i> without truncation and the buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cchDest</i> is either 0 or larger than <b>STRSAFE_MAX_CCH</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed due to insufficient buffer space. The destination buffer contains a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
</table>
 




## -remarks



For more information on va_lists, see the conventions defined in Stdarg.h.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="https://docs.microsoft.com/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintf_lexa">StringCchVPrintf_lEx</a> if you require the handling of null string pointer values.

In order to use this function, you must define the following macro in your header file, before including StrSafe.h.

<code>#define STRSAFE_LOCALE_FUNCTIONS</code>



