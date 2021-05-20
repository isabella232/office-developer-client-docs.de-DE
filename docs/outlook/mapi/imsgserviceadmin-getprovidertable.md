---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428767"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Anbietertabelle, eine Auflistung der Dienstanbieter im Profil.
  
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
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::GetProviderTable-Methode** bietet Zugriff auf die MAPI-Anbietertabelle, eine Tabelle, in der alle derzeit im Profil installierten Adressbuch-, Nachrichtenspeicher- und Transportanbieter aufgeführt sind. 
  
Im Gegensatz zur über die [IProviderAdmin::GetProviderTable-Methode](iprovideradmin-getprovidertable.md) zurückgegebenen Anbietertabelle kann die über **IMsgServiceAdmin::GetProviderTable** zurückgegebene Anbietertabelle keine zusätzlichen Zeilen enthalten, die Informationen darstellen, die einem oder mehreren Dienstanbietern im Profil zugeordnet sind. 
  
Anbieter, die gelöscht wurden oder verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Anbietertabelle enthalten. Anbietertabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Profil nicht in der Tabelle enthalten sind. 
  
Wenn das Profil keine Anbieter enthält, gibt **GetProviderTable** eine Tabelle mit null Zeilen und dem Rückgabewert S_OK zurück. 
  
Eine vollständige Liste der Spalten in der Anbietertabelle finden Sie unter [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie das folgende Verfahren, um die Zeilen einer Anbietertabelle in Transportreihenfolge abzurufen:
  
1. Rufen Sie die [IMAPITable::Restrict-Methode](imapitable-restrict.md) auf, um eine Eigenschaftseinschränkung aufzuerzwingen, die der **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) -Eigenschaft mit MAPI_TRANSPORT_PROVIDER.
    
2. Rufen Sie die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) auf, um die Tabelle nach der Spalte **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) zu sortieren. 
    
3. Rufen Sie [die IMAPITable::QueryRows-Methode](imapitable-queryrows.md) auf, um die Zeilen der Tabelle zu erhalten. 
    
Eine Alternative zu diesen Aufrufen besteht in einem einzigen Aufruf der [HrQueryAllRows-Funktion,](hrqueryallrows.md) bei dem alle entsprechenden Datenstrukturen übergeben werden. 
  
Wenn Sie die **spalten PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) in jeder Zeile abrufen, können Sie dieses Array von **MAPIUID-Strukturen** verwenden, um die Transportreihenfolge in einem Aufruf von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)festlegen.
  
Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ führt folgendes aus: 
  
- Legt den Zeichenfolgentyp auf Unicode für Daten fest, die für die anfänglichen aktiven Spalten der Anbietertabelle von der [IMAPITable::QueryColumns-Methode zurückgegeben](imapitable-querycolumns.md) werden. Die anfänglichen aktiven Spalten für eine Anbietertabelle sind die Spalten, die die **QueryColumns-Methode** zurückgibt, bevor der Anbieter, der die Tabelle enthält, die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) aufruft. 
    
- Legt den Zeichenfolgentyp auf Unicode für Daten fest, die für die anfänglichen aktiven Zeilen der Anbietertabelle von **QueryRows zurückgegeben werden.** Die ersten aktiven Zeilen für eine Anbietertabelle sind die Zeilen, die **QueryRows** vor dem Anbieter zurückgibt, der die Tabelle enthält, aufruft **SetColumns**. 
    
- Steuert die Eigenschaftstypen der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird, bevor der Client, der die Anbietertabelle enthält, die [IMAPITable::SortTable-Methode](imapitable-sorttable.md) aufruft. 
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

