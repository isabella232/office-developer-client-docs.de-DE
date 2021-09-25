---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 34cfe5f263efea1f7366cc271656be626f15bb8a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630789"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert die aktuelle Nachricht in einen Ordner.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parameter

 _pFolderDestination_
  
> [in] Ein Zeiger auf den Ordner, in den die Nachricht kopiert werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIMessageSite::CopyMessage-Methode** auf, um die aktuelle Nachricht in einen neuen Ordner zu kopieren. **CopyMessage** ändert die Nachricht, die dem Benutzer derzeit angezeigt wird, nicht, und es wird keine Benutzeroberfläche für die neu erstellte Nachricht an das Formular zurückgegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine typische Implementierung der **CopyMessage-Methode** führt die folgenden Aufgaben aus: 
  
1. Erstellt eine neue Nachricht für die aktuelle Nachricht, in die kopiert werden soll.
    
2. Ruft die [IPersistMessage::Save-Methode](ipersistmessage-save.md) mit einem Zeiger auf die neue Nachricht im  _pMessage-Parameter_ und FALSE im  _fSameAsLoad-Parameter_ auf. 
    
3. Ruft die [IPersistMessage::SaveCompleted-Methode](ipersistmessage-savecompleted.md) auf und übergibt NULL im _pMessage-Parameter._ 
    
4. Ruft die [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) für die neue Nachricht auf. 
    
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI-Formularschnittstellen.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

