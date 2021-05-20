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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430000"
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
    
## <a name="remarks"></a>Hinweise

Form-Objekte rufen die **IMAPIMessageSite::CopyMessage-Methode** auf, um die aktuelle Nachricht in einen neuen Ordner zu kopieren. **CopyMessage** ändert die Nachricht, die dem Benutzer derzeit angezeigt wird, nicht, und es wird keine Schnittstelle für die neu erstellte Nachricht an das Formular zurückgegeben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Eine typische Implementierung der **CopyMessage-Methode** führt die folgenden Aufgaben aus: 
  
1. Erstellt eine neue Nachricht, in die die aktuelle Nachricht kopiert werden soll.
    
2. Ruft die [IPersistMessage::Save-Methode](ipersistmessage-save.md) mit einem Zeiger auf die neue Nachricht im  _pMessage-Parameter_ und FALSE im  _fSameAsLoad-Parameter_ auf. 
    
3. Ruft die [IPersistMessage::SaveCompleted-Methode](ipersistmessage-savecompleted.md) auf, und übergeben Sie NULL im _pMessage-Parameter._ 
    
4. Ruft die [IMAPIProp::SaveChanges-Methode für](imapiprop-savechanges.md) die neue Nachricht auf. 
    
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).
  
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

