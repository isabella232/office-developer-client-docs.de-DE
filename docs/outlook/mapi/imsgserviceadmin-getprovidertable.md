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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317381"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Anbieter Tabelle, eine Liste der Dienstanbieter im Profil.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Immer NULL.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Anbieter Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anbieter Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin:: GetProvider** Table-Methode ermöglicht den Zugriff auf die MAPI-Anbieter Tabelle, eine Tabelle, in der das gesamte Adressbuch, der Nachrichtenspeicher und die Transportanbieter aufgelistet sind, die aktuell im Profil installiert sind. 
  
Im Gegensatz zur Anbieter Tabelle, die über die [IProviderAdmin:: GetProvider](iprovideradmin-getprovidertable.md) Table-Methode zurückgegeben wird, kann die durch **IMsgServiceAdmin::** getproviderable zurückgegebene Anbieter Tabelle keine zusätzlichen Zeilen mit zugeordneten Informationen darstellen. mit einem oder mehreren Dienstanbietern im Profil. 
  
Anbieter, die gelöscht oder verwendet wurden, aber zum Löschen markiert wurden, sind nicht in der Anbieter Tabelle enthalten. Anbieter Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Profil nicht in der Tabelle wiedergegeben werden. 
  
Wenn das Profil keine Anbieter hat, **** gibt getproviderable eine Tabelle mit null Zeilen und dem RÜCKGABEwert S_OK zurück. 
  
Eine vollständige Liste der Spalten in der Anbieter Tabelle finden Sie unter [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Gehen Sie folgendermaßen vor, um die Zeilen einer Anbieter Tabelle in der Transport Reihenfolge abzurufen:
  
1. Rufen Sie die [IMAPITable:: Restrict](imapitable-restrict.md) -Methode auf, um eine Eigenschaftseinschränkung aufzuerlegen, die der **PR_RESOURCE_TYPE** ([PIDTAGRESOURCETYPE (](pidtagresourcetype-canonical-property.md))-Eigenschaft mit MAPI_TRANSPORT_PROVIDER entspricht.
    
2. Rufen Sie die [IMAPITable:: sortable](imapitable-sorttable.md) -Methode auf, um die Tabelle nach der **PR_PROVIDER_ORDINAL** ([pidtagproviderordinal (](pidtagproviderordinal-canonical-property.md))-Spalte zu sortieren. 
    
3. Rufen Sie die [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode auf, um die Zeilen der Tabelle abzurufen. 
    
Eine Alternative zu diesen Aufrufen besteht darin, einen einzelnen Aufruf der [HrQueryAllRows](hrqueryallrows.md) -Funktion mit allen entsprechenden Datenstrukturen vorzunehmen. 
  
Wenn Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Spalten in den einzelnen Zeilen abrufen, können Sie dieses Array von **MAPIUID** -Strukturen zum Festlegen der Transport Reihenfolge in einem Aufruf von [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)verwenden.
  
Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter führt zu folgenden Aktionen: 
  
- Legt den Zeichenfolgentyp für Daten fest, die für die anfänglichen aktiven Spalten der Anbieter Tabelle von der [IMAPITable:: QueryColumns](imapitable-querycolumns.md) -Methode zurückgegeben werden. Die ersten aktiven Spalten für eine Anbieter Tabelle sind die Spalten, die die **QueryColumns** -Methode zurückgibt, bevor der Anbieter, der die Tabelle enthält, die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode aufruft. 
    
- Legt den Zeichenfolgentyp auf Unicode für Daten fest, die für die anfänglichen aktiven Zeilen der Anbieter Tabelle von **QueryRows**zurückgegeben werden. Die ersten aktiven Zeilen für eine Anbieter Tabelle sind die Zeilen, die **QueryRows** zurückgibt, bevor der Anbieter, der die Tabelle enthält, SetColumns aufruft. **** 
    
- Steuert die Eigenschaftentypen der Sortierreihenfolge, die von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben wird, bevor der Client, der die Anbieter Tabelle enthält, die [IMAPITable:: sortable](imapitable-sorttable.md) -Methode aufruft. 
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

