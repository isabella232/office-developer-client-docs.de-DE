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
ms.openlocfilehash: 843a61696def4398c22a244a7f3f66d7e5dc75ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279528"
---
# <a name="iprovideradmingetprovidertable"></a>IProviderAdmin::GetProviderTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ermöglicht den Zugriff auf die Anbieter Tabelle des Nachrichtendiensts, eine Liste der Dienstanbieter im Nachrichtendienst.
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der in den Spalten der Anbieter Tabelle zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Spalten im ANSI-Format.
    
 _lppTable_
  
> Out Ein Zeiger auf einen Zeiger auf die Anbieter Tabelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anbieter Tabelle wurde erfolgreich zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IProviderAdmin::** getproviderable-Methode ruft einen Zeiger auf die Anbieter Tabelle des Nachrichtendiensts ab, eine Tabelle, die von MAPI verwaltet wird und die Informationen zu jedem Dienstanbieter im Nachrichtendienst enthält. 
  
Im Gegensatz zur Anbieter Tabelle, die von der [IMsgServiceAdmin:: GetProvider](imsgserviceadmin-getprovidertable.md) Table-Methode zurückgegeben wird, kann die von **IProviderAdmin::** getproviderable zurückgegebene Anbieter Tabelle zusätzliche Zeilen mit Informationen darstellen, die einer oder mehreren der die Dienstanbieter im Nachrichtendienst. Diese zusätzlichen Informationen werden dem Profil mit dem Schlüsselwort "Sections" der Datei MAPISVC. inf hinzugefügt. Wenn ein Anbieter über zusätzliche Profilabschnitte verfügt, werden die **MAPIUID** -Strukturen für diese Abschnitte in der **PR_SERVICE_EXTRA_UIDS** ([pidtagserviceextrauids (](pidtagserviceextrauids-canonical-property.md))-Eigenschaft gespeichert. **PR_SERVICE_EXTRA_UIDS** wird im Abschnitt Nachrichtendienst Profil gespeichert. 
  
Anbieter, die gelöscht oder verwendet wurden, aber zum Löschen markiert wurden, sind nicht in der Anbieter Tabelle enthalten. Anbieter Tabellen sind statisch, was bedeutet, dass nachfolgende Ergänzungen oder Löschungen aus dem Nachrichtendienst nicht in der Tabelle wiedergegeben werden. 
  
Wenn der Nachrichtendienst keine Anbieter hat, gibt **IProviderAdmin::** getproviderable eine Tabelle mit null Zeilen und dem RÜCKGABEwert S_OK zurück. 
  
Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable:: QueryColumns](imapitable-querycolumns.md) und [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegeben werden. 
  
Dieses Flag steuert auch die Eigenschaftentypen in der von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegebenen Sortierreihenfolge. 
  
Eine vollständige Liste der Spalten in der Anbieter Tabelle finden Sie unter [Provider Table](provider-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um die Zeilen einer Anbieter Tabelle in der Transport Reihenfolge abzurufen, Sortieren Sie die Tabelle nach der **PR_PROVIDER_ORDINAL** ([pidtagproviderordinal (](pidtagproviderordinal-canonical-property.md))-Spalte. 
  
Um nur die Zeilen abzurufen, die Dienstanbieter darstellen (ohne zusätzliche Zeilen), begrenzen Sie Ihren Abruf auf die Zeilen mit dem Wert PT_ERROR in der **PR_RESOURCE_TYPE** ([pidtagresourcetype (](pidtagresourcetype-canonical-property.md))-Spalte.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
| MsgServiceTableDlg. cpp  <br/> |CMsgServiceTableDlg:: OnDisplayItem  <br/> |MFCMAPI verwendet die **IProviderAdmin:: GetProvider** Table-Methode, um die Tabelle der Anbieter abzurufen, die in einem neuen Dialogfeld gerendert werden sollen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

