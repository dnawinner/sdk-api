---
UID: NS:ntdsapi.__unnamed_struct_8
title: DS_REPSYNCALL_UPDATEA (ntdsapi.h)
description: The DS_REPSYNCALL_UPDATE structure contains status data about the replication performed by the DsReplicaSyncAll function.helpviewer_keywords: ["*PDS_REPSYNCALL_UPDATEA","DS_REPSYNCALL_UPDATE","DS_REPSYNCALL_UPDATE structure [Active Directory]","DS_REPSYNCALL_UPDATEA","DS_REPSYNCALL_UPDATEW","PDS_REPSYNCALL_UPDATE","PDS_REPSYNCALL_UPDATE structure pointer [Active Directory]","_glines_ds_repsyncall_update","ad.ds__repsyncall__update","ad.ds_repsyncall_update","ntdsapi/DS_REPSYNCALL_UPDATE","ntdsapi/DS_REPSYNCALL_UPDATEA","ntdsapi/DS_REPSYNCALL_UPDATEW","ntdsapi/PDS_REPSYNCALL_UPDATE"]
old-location: ad\ds_repsyncall_update.htm
tech.root: ad
ms.assetid: 3b0005cb-0fb6-492c-89e5-8a18a88f881b
ms.date: 12/05/2018
ms.keywords: '*PDS_REPSYNCALL_UPDATEA, DS_REPSYNCALL_UPDATE, DS_REPSYNCALL_UPDATE structure [Active Directory], DS_REPSYNCALL_UPDATEA, DS_REPSYNCALL_UPDATEW, PDS_REPSYNCALL_UPDATE, PDS_REPSYNCALL_UPDATE structure pointer [Active Directory], _glines_ds_repsyncall_update, ad.ds__repsyncall__update, ad.ds_repsyncall_update, ntdsapi/DS_REPSYNCALL_UPDATE, ntdsapi/DS_REPSYNCALL_UPDATEA, ntdsapi/DS_REPSYNCALL_UPDATEW, ntdsapi/PDS_REPSYNCALL_UPDATE'
f1_keywords:
- ntdsapi/DS_REPSYNCALL_UPDATE
dev_langs:
- c++
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_REPSYNCALL_UPDATEW (Unicode) and DS_REPSYNCALL_UPDATEA (ANSI)
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
- Ntdsapi.h
api_name:
- DS_REPSYNCALL_UPDATE
- DS_REPSYNCALL_UPDATEA
- DS_REPSYNCALL_UPDATEW
targetos: Windows
req.typenames: DS_REPSYNCALL_UPDATEA, *PDS_REPSYNCALL_UPDATEA
req.redist: 
ms.custom: 19H1
---

# DS_REPSYNCALL_UPDATEA structure


## -description


The <b>DS_REPSYNCALL_UPDATE</b> structure contains status data about the replication performed by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a> function. The <b>DsReplicaSyncAll</b> function passes this structure to a callback function in its <i>pFnCallBack</i> parameter. For more information about the callback function, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms677968(v=vs.85)">SyncUpdateProc</a>.


## -struct-fields




### -field event

Contains a <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repsyncall_event">DS_REPSYNCALL_EVENT</a> value that describes the event which the <b>DS_REPSYNCALL_UPDATE</b> structure represents.


### -field pErrInfo

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a> structure that contains error data about the replication performed by the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a> function.


### -field pSync

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_synca">DS_REPSYNCALL_SYNC</a> structure that identifies the source and destination servers that have either initiated or finished synchronization.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa">DS_REPSYNCALL_ERRINFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ne-ntdsapi-ds_repsyncall_event">DS_REPSYNCALL_EVENT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_repsyncall_synca">DS_REPSYNCALL_SYNC</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsreplicasyncalla">DsReplicaSyncAll</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms677968(v=vs.85)">SyncUpdateProc</a>
 

 

