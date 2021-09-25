---
title: IProviderAdminGetProviderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProviderAdmin.GetProviderTable
api_type:
- COM
ms.assetid: e9deaa7c-430b-4e97-8ed6-f7c615956e0f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28025b2b60ebb563064fd3960df5a5057aea97ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561376"
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
  
> [in] Eine Bitmaske mit Flags, die den Typ der Zeichenfolgen steuert, die in den Spalten der Anbietertabelle zurückgegeben werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Spalten das ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Anbietertabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anbietertabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IProviderAdmin::GetProviderTable-Methode** ruft einen Zeiger auf die Anbietertabelle des Nachrichtendiensts ab, eine Tabelle, die mapi verwaltet, die Informationen zu jedem Dienstanbieter im Nachrichtendienst enthält. 
  
Im Gegensatz zur von der [IMsgServiceAdmin::GetProviderTable-Methode](imsgserviceadmin-getprovidertable.md) zurückgegebenen Anbietertabelle kann die von **IProviderAdmin::GetProviderTable** zurückgegebene Anbietertabelle zusätzliche Zeilen enthalten, die Informationen darstellen, die einem oder mehreren der Dienstanbieter im Nachrichtendienst zugeordnet sind. Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" der Datei Mapisvc.inf hinzugefügt. Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, werden die **MAPIUID-Strukturen** für diese Abschnitte in der **Eigenschaft PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) gespeichert. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt "Nachrichtendienstprofil" gespeichert. 
  
Anbieter, die gelöscht wurden oder verwendet werden, aber für den Löschvorgang markiert wurden, sind nicht in der Anbietertabelle enthalten. Anbietertabellen sind statisch, d. h., nachfolgende Ergänzungen oder Löschungen aus dem Nachrichtendienst werden in der Tabelle nicht widergespiegelt. 
  
Wenn der Nachrichtendienst keine Anbieter hat, gibt **IProviderAdmin::GetProviderTable** eine Tabelle mit null Zeilen und dem S_OK Rückgabewert zurück. 
  
Das Festlegen des MAPI_UNICODE Flags im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden. 
  
Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode](imapitable-querysortorder.md) zurückgegeben wird. 
  
Eine vollständige Liste der Spalten in der Anbietertabelle finden Sie unter [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die Zeilen einer Anbietertabelle in Transportreihenfolge abzurufen, sortieren Sie die Tabelle nach der **Spalte PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)). 
  
Um nur die Zeilen abzurufen, die Dienstanbieter darstellen (ohne zusätzliche Zeilen einzuschn?nen), beschränken Sie den Abruf auf die Zeilen, die den Wert PT_ERROR in der **spalte PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) aufweisen.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
| MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI verwendet die **IProviderAdmin::GetProviderTable-Methode,** um die Tabelle der Anbieter abzurufen, die in einem neuen Dialogfeld gerendert werden sollen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

