---
UID: NF:tapi3.IEnumQueue.Clone
title: IEnumQueue::Clone (tapi3.h)
description: The Clone method creates another enumerator that contains the same enumeration state as the current one.helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumQueue interface","IEnumQueue interface [TAPI 2.2]","Clone method","IEnumQueue.Clone","IEnumQueue::Clone","_tapi3_ienumqueue_clone","tapi3.ienumqueue_clone","tapi3cc/IEnumQueue::Clone"]
old-location: tapi3\ienumqueue_clone.htm
tech.root: Tapi
ms.assetid: e63df5aa-8c90-4978-a63f-96ac5f624ef4
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumQueue interface, IEnumQueue interface [TAPI 2.2],Clone method, IEnumQueue.Clone, IEnumQueue::Clone, _tapi3_ienumqueue_clone, tapi3.ienumqueue_clone, tapi3cc/IEnumQueue::Clone
f1_keywords:
- tapi3/IEnumQueue.Clone
dev_langs:
- c++
req.header: tapi3.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- IEnumQueue.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumQueue::Clone


## -description


The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppEnum [out]

Pointer to new 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumqueue">IEnumQueue</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnum</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumqueue">IEnumQueue</a> interface returned by <b>IEnumQueue::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumQueue</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-ienumqueue">IEnumQueue</a>
 

 

