---
UID: NC:winbio_adapter.PIBIO_ENGINE_ACTIVATE_FN
title: PIBIO_ENGINE_ACTIVATE_FN (winbio_adapter.h)
description: Gives the Engine Adapter the chance to perform any work needed to bring the sensor component out of an idle state.helpviewer_keywords: ["EngineAdapterActivate","EngineAdapterActivate callback function [Windows Biometric Framework API]","PIBIO_ENGINE_ACTIVATE_FN","PIBIO_ENGINE_ACTIVATE_FN callback","secbiomet.engineadapteractivate","winbio_adapter/EngineAdapterActivate"]
old-location: secbiomet\engineadapteractivate.htm
tech.root: SecBioMet
ms.assetid: 0E98D887-A974-4B86-934E-939DEB1946DF
ms.date: 12/05/2018
ms.keywords: EngineAdapterActivate, EngineAdapterActivate callback function [Windows Biometric Framework API], PIBIO_ENGINE_ACTIVATE_FN, PIBIO_ENGINE_ACTIVATE_FN callback, secbiomet.engineadapteractivate, winbio_adapter/EngineAdapterActivate
f1_keywords:
- winbio_adapter/EngineAdapterActivate
dev_langs:
- c++
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- EngineAdapterActivate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_ENGINE_ACTIVATE_FN callback function


## -description


Called by the Windows Biometric Framework to give the Engine Adapter the chance to perform any work needed to bring the sensor component out of an idle state.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method is called when the first client session opens a handle to an inactive biometric unit.

The Storage adapter has been activated when this method is called.

Returning any <b>HRESULT</b> other than <b>S_OK</b> will cause the Windows Biometric Framework to log the error and abort the activation of the biometric unit.

This method executes in the context of the sensor control thread that will process all other requests for the unit, including deactivation.



