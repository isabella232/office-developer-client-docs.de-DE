---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bc20d10e20a170a12d30053e35c79718ac088db1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567284"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Anbietertabelle, eine Auflistung der Dienstanbieter im Profil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Immer NULL.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Anbietertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anbietertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::GetProviderTable-Methode** ermöglicht den Zugriff auf die MAPI-Anbietertabelle, eine Tabelle, in der alle derzeit im Profil installierten Adressbuch-, Nachrichtenspeicher- und Transportanbieter aufgeführt sind. 
  
Im Gegensatz zur über die [IProviderAdmin::GetProviderTable-Methode](iprovideradmin-getprovidertable.md) zurückgegebenen Anbietertabelle kann die über **IMsgServiceAdmin::GetProviderTable** zurückgegebene Anbietertabelle keine zusätzlichen Zeilen enthalten, die Informationen darstellen, die einem oder mehreren Dienstanbietern im Profil zugeordnet sind. 
  
Anbieter, die gelöscht wurden oder verwendet werden, aber für den Löschvorgang markiert wurden, sind nicht in der Anbietertabelle enthalten. Anbietertabellen sind statisch, d. h., nachfolgende Ergänzungen oder Löschungen aus dem Profil werden in der Tabelle nicht widergespiegelt. 
  
Wenn das Profil über keine Anbieter verfügt, gibt **GetProviderTable** eine Tabelle mit null Zeilen und dem S_OK Rückgabewert zurück. 
  
Eine vollständige Liste der Spalten in der Anbietertabelle finden Sie unter [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Gehen Sie folgendermaßen vor, um die Zeilen einer Anbietertabelle in Transportreihenfolge abzurufen:
  
1. Rufen Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) auf, um eine Eigenschaftseinschränkung aufzuerlegen, die der **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) -Eigenschaft mit MAPI_TRANSPORT_PROVIDER entspricht.
    
2. Rufen Sie die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) auf, um die Tabelle nach der **Spalte PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) zu sortieren. 
    
3. Rufen Sie die [IMAPITable::QueryRows-Methode](imapitable-queryrows.md) auf, um die Zeilen der Tabelle abzurufen. 
    
Eine Alternative zu diesen Aufrufen ist ein einzelner Aufruf der [HrQueryAllRows-Funktion](hrqueryallrows.md) mit allen übergebenen entsprechenden Datenstrukturen. 
  
Wenn Sie die **Spalten PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) in jeder der Zeilen abrufen, können Sie dieses Array von **MAPIUID-Strukturen** verwenden, um die Transportreihenfolge in einem Aufruf von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)festzulegen.
  
Durch Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wird Folgendes ausgeführt: 
  
- Legt den Zeichenfolgentyp für Daten, die von der [IMAPITable::QueryColumns-Methode](imapitable-querycolumns.md) für die anfänglichen aktiven Spalten der Anbietertabelle zurückgegeben werden, auf Unicode fest. Die anfänglich aktiven Spalten für eine Anbietertabelle sind die Spalten, die die **QueryColumns-Methode** zurückgibt, bevor der Anbieter, der die Tabelle enthält, die [IMAPITable::SetColumns-Methode aufruft.](imapitable-setcolumns.md) 
    
- Legt den Zeichenfolgentyp auf Unicode für Daten fest, die von **QueryRows** für die anfänglichen aktiven Zeilen der Anbietertabelle zurückgegeben werden. Die anfänglich aktiven Zeilen für eine Anbietertabelle sind die Zeilen, die **QueryRows** zurückgibt, bevor der Anbieter, der die Tabelle **enthält, SetColumns aufruft.** 
    
- Steuert die Eigenschaftstypen der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird, bevor der Client, der die Anbietertabelle enthält, die [IMAPITable::SortTable-Methode aufruft.](imapitable-sorttable.md) 
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

