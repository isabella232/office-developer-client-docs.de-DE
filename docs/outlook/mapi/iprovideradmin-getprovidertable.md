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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434473"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bietet Zugriff auf die Anbietertabelle des Nachrichtendiensts, eine Liste der Dienstanbieter im Nachrichtendienst.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der in den Spalten der Anbietertabelle zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Spalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Anbietertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anbietertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Die **IProviderAdmin::GetProviderTable-Methode** ruft einen Zeiger auf die Anbietertabelle des Nachrichtendiensts ab, eine Tabelle, die MAPI verwaltet, die Informationen zu den einzelnen Dienstanbietern im Nachrichtendienst enthält. 
  
Im Gegensatz zur von der [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) zurückgegebenen Anbietertabelle kann die von **IProviderAdmin::GetProviderTable** zurückgegebene Anbietertabelle zusätzliche Zeilen enthalten, die Informationen darstellen, die einem oder mehreren Dienstanbietern im Nachrichtendienst zugeordnet sind. Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" der Datei Mapisvc.inf hinzugefügt. Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, speichert er die **MAPIUID-Strukturen** für diese Abschnitte in der **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) -Eigenschaft. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Nachrichtendienstprofil gespeichert. 
  
Anbieter, die gelöscht wurden oder verwendet werden, aber zum Löschen markiert wurden, sind nicht in der Anbietertabelle enthalten. Anbietertabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Nachrichtendienst nicht in der Tabelle enthalten sind. 
  
Wenn der Nachrichtendienst über keine Anbieter verfügt, gibt **IProviderAdmin::GetProviderTable** eine Tabelle mit null Zeilen und dem Rückgabewert S_OK zurück. 
  
Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. 
  
Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird. 
  
Eine vollständige Liste der Spalten in der Anbietertabelle finden Sie unter [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die Zeilen einer Anbietertabelle in Transportreihenfolge abzurufen, sortieren Sie die Tabelle nach der spalte **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Um nur die Zeilen abzurufen, die Dienstanbieter darstellen (ohne zusätzliche Zeilen), beschränken Sie den Abruf auf die Zeilen, die den Wert PT_ERROR in der Spalte **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) haben.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI verwendet die **IProviderAdmin::GetProviderTable-Methode,** um die Tabelle der Anbieter zum Rendern in einem neuen Dialogfeld zu erhalten.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

