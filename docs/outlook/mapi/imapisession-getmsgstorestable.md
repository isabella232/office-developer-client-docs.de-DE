---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792299"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Betrifft**: Outlook 
  
Bietet Zugriff auf die Nachricht Store Tabelle mit Informationen zu allen Nachrichtenspeichern im Profil der Sitzung.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die bestimmt das Format für Spalten, die Zeichenfolgen sind. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgenspalten sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.
    
 _lppTable_
  
> [out] Ein Zeiger auf einen Zeiger auf die Nachricht Store-Tabelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Tabelle wurde erfolgreich zurückgegeben.
    
MAPI_E_BAD_CHARWIDTH 
  
> Die Option MAPI_UNICODE wurde festgelegt, und die Sitzung Unicode nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISession::GetMsgStoresTable** -Methode ruft einen Zeiger auf die Nachricht Store-Tabelle, eine Tabelle von MAPI verwaltet wird, enthält Informationen zu jeder geöffneten Nachrichtenspeicher im Profil. 
  
Speichern Sie eine vollständige Liste der erforderlichen und optionalen Spalten in der Nachricht Tabelle, finden Sie unter [Nachricht speichern Tabellen](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da MAPI die Tabelle Store während der Sitzung aktualisiert immer Änderungen auftreten, rufen Sie die **Advise** -Methode der Nachricht Store Tabelle registrieren, um diese Änderungen benachrichtigt werden. Mögliche Änderungen zählen das Hinzufügen von neuen Nachrichtenspeicher, Entfernen vorhandener speichert und in der Standard-Informationsspeichers geändert. 
  
Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus. Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI (engl.) verwendet die **IMAPISession::GetMsgStoresTable** -Methode, um die Nachricht Store-Tabelle zu erhalten, damit es im Hauptdialogfeld von MFCMAPI (engl.) gerendert werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Nachrichtenspeichertabellen](message-store-tables.md)

