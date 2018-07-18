---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2ad57b91a1b9d06ab8284fa53c283d17e4eb5613
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792790"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Betrifft**: Outlook 
  
Bietet Zugriff auf den Dienst Anbieter Tabelle, eine Liste der Dienstanbieter in der Nachrichtendienst.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ der Zeichenfolgen in der Anbieter Tabellenspalten zurückgegeben steuert. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Spalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf den Anbieter-Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anbieter Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IProviderAdmin::GetProviderTable** -Methode ruft einen Zeiger auf den Dienst Anbieter Tabelle, einer Tabelle, die MAPI verwaltet, die Informationen zu jeder Dienstanbieter im Nachrichtendienst enthält. 
  
Im Gegensatz zu der Provider-Tabelle zurückgegeben, die von der [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) -Methode kann die Provider-Tabelle **IProviderAdmin::GetProviderTable** zurückgegebene zusätzliche Zeilen enthalten, die Informationen im Zusammenhang mit mindestens einem darstellen der Dienstanbieter in der Nachrichtendienst. Diese zusätzlichen Informationen wird das Profil mit dem Schlüsselwort "Abschnitte", der die Datei "Mapisvc.inf" hinzugefügt. Wenn ein Anbieter zusätzliche Profil hat, werden die **MAPIUID** Strukturen für diese Abschnitte in der Eigenschaft **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) gespeichert. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Profile Service Nachricht gespeichert. 
  
Anbieter, die gelöscht wurden, oder verwendet werden, doch zum Löschen markiert wurden, sind nicht in der Provider-Tabelle enthalten. Provider-Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschvorgänge aus den Dienst in der Tabelle nicht wiedergegeben werden. 
  
Wenn der Nachrichtendienst keine Anbieter ist, gibt **IProviderAdmin::GetProviderTable** eine Tabelle mit 0 (null) Zeilen und der Wert S_OK zurückgegeben. 
  
Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus. 
  
Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben. 
  
Eine vollständige Liste der Spalten in der Tabelle Anbieter finden Sie unter [Provider-Tabelle](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie die Zeilen einer Tabelle Anbieter in der Reihenfolge der Transport sortieren Sie die Tabelle nach der Spalte **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Einschränken Sie, um nur die Zeilen abrufen, die Dienstanbieter darstellen (ohne zusätzlichen Zeilen), Ihre Abruf auf die Zeilen, die den Wert in der Spalte **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) PT_ERROR haben.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI (engl.) verwendet die **IProviderAdmin::GetProviderTable** -Methode zum Abrufen der Tabelle der Anbieter in ein neues Dialogfeld gerendert werden soll.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

