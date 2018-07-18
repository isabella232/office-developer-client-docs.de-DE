---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5bf2ff74f6cda01608efd4b372aa4b03468c820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792204"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**Betrifft**: Outlook 
  
Kopiert die aktuelle Nachricht in einen Ordner.
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>Parameter

 _pFolderDestination_
  
> [in] Ein Zeiger auf den Ordner, in dem die Nachricht kopiert werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Site Nachricht nicht unterstützt.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte Aufrufen die **IMAPIMessageSite::CopyMessage** -Methode, um die aktuelle Nachricht in einen neuen Ordner zu kopieren. **CopyMessage** ändert nicht die Nachricht an den Benutzer derzeit angezeigt wird, und keine Schnittstelle für die neu erstellte Nachricht an das Formular zurückgegeben wird. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine typische Implementierung der **CopyMessage** -Methode führt die folgenden Aufgaben: 
  
1. Erstellt eine neue Nachricht für die aktuelle Nachricht in kopiert werden.
    
2. Ruft die [IPersistMessage::Save](ipersistmessage-save.md) -Methode mit einem Zeiger auf die neue Nachricht in den _pMessage_ -Parameter und FALSE im _fSameAsLoad_ -Parameter. 
    
3. Ruft die [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode NULL im _pMessage_ -Parameter übergeben. 
    
4. Ruft die [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode auf die neue Nachricht an. 
    
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern, finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularoberflächen](mapi-form-interfaces.md)

