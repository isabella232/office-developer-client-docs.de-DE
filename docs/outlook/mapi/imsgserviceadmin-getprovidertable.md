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
ms.openlocfilehash: 834b010dc4810e26264bb418de9630bc83b99810
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565291"
---
# <a name="imsgserviceadmingetprovidertable"></a>IMsgServiceAdmin::GetProviderTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Tabelle Dienstanbieter, eine Liste der Dienstanbieter im Profil.
  
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
  
> [out] Ein Zeiger auf einen Zeiger auf den Anbieter-Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anbieter Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::GetProviderTable** -Methode ermöglicht den Zugriff auf die MAPI-Anbieter-Tabelle eine Tabelle, die alle Adressbuch, Nachrichtenspeicher und Transportanbieter, die derzeit im Profil installiert aufgeführt sind. 
  
Im Gegensatz zu der Tabelle der Dienstanbieter über die [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) -Methode zurückgegeben kann nicht die Anbieter zurückgegebenen **IMsgServiceAdmin::GetProviderTable** zusätzliche Zeilen einzubeziehen, die Informationen im Zusammenhang darstellen mit mindestens -Dienstanbietern im Profil 
  
Anbieter, die gelöscht wurden, oder verwendet werden, doch zum Löschen markiert wurden, sind nicht in der Provider-Tabelle enthalten. Provider-Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschvorgänge aus dem Profil in der Tabelle nicht wiedergegeben werden. 
  
Wenn das Profil keine Anbieter aufweist, gibt **GetProviderTable** eine Tabelle mit 0 (null) Zeilen und den Rückgabewert S_OK zurück. 
  
Eine vollständige Liste der Spalten in der Tabelle Anbieter finden Sie unter [Provider-Tabelle](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die Zeilen einer Tabelle Anbieter in Transport Reihenfolge verwenden Sie die folgende Schritte aus:
  
1. Rufen Sie die [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode, um eine eigenschaftseinschränkung zugrunde liegen, die die **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))-Eigenschaft mit MAPI_TRANSPORT_PROVIDER entspricht.
    
2. Aufrufen der [SortTable](imapitable-sorttable.md) -Methode, um die Tabelle nach der **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))-Spalte zu sortieren. 
    
3. Rufen Sie [die QueryRows, um die Zeilen der Tabelle zu erhalten](imapitable-queryrows.md) . 
    
Eine Alternative zu diesen anrufen ist auf einen einzigen Aufruf der Funktion [HrQueryAllRows](hrqueryallrows.md) mit aller entsprechenden Daten ansetzen, die Strukturen in übergeben. 
  
Wenn Sie die Spalten **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) in den einzelnen Zeilen abrufen, können Sie dieses Array von **MAPIUID** -Strukturen, die Transport-Reihenfolge in einem Aufruf von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)festgelegt.
  
Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ bewirkt Folgendes: 
  
- Legt den Typ String in Unicode für von der [IMAPITable::QueryColumns](imapitable-querycolumns.md) -Methode für die anfänglichen aktiven Spalten der Tabelle vom Anbieter zurückgegebenen Daten fest. Die ersten aktiven Spalten für eine Tabelle Anbieter sind die Spalten, die die **QueryColumns** -Methode vor der Anbieter zurückgibt, die die Tabelle Aufrufe die [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode enthält. 
    
- Legt den Typ String in Unicode für von **QueryRows**für die anfänglichen aktiven Zeilen der Tabelle vom Anbieter zurückgegebenen Daten fest. Die anfänglichen aktiven Zeilen, die für eine Anbieter-Tabelle sind die Zeilen, die **QueryRows** vor der Anbieter zurückgibt, das die Tabelle Aufrufe **SetColumns**enthält. 
    
- Steuert die Eigenschaftentypen der Sortierreihenfolge von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben wird, bevor der Client, der die Anbieter-Tabelle enthält die [SortTable](imapitable-sorttable.md) -Methode aufruft. 
    
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)
  
[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

