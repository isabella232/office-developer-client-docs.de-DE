---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8cf28a3c5b6cdcfc8873a9613ac1fef2b5e7640a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579929"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigenden Nachricht verarbeiten kann.
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Parameter

 _lpszMessageClass_
  
> [in] Ein Zeiger auf die Nachrichtenklasse der nächsten Nachricht.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske mit client- oder anbieterdefinierten Flags, die aus der **eigenschaft PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) der nächsten anzuzeigenden Nachricht kopiert wird und Statusinformationen zum Inhaltsverzeichnis bereitstellt, in dem die Nachricht enthalten ist.
    
 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske mit Flags, die aus der **eigenschaft PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der nächsten Nachricht kopiert wurden, um den aktuellen Status der Nachricht anzuzeigen.
    
 _ppPersistMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die [IPersistMessage-Implementierung](ipersistmessageiunknown.md) für das Formularobjekt, das für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist. Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt zum Anzeigen und Speichern der nächsten Nachricht verwendet werden kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.
    
S_FALSE 
  
> Das Formular behandelt nicht die Nachrichtenklasse der nächsten Nachricht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIFormAdviseSink::OnActivateNext-Methode auf,** um dem Formular zu helfen, zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden kann. Die nächste Nachricht kann eine Nachricht einer beliebigen Klasse sein, aber in der Regel entspricht sie derselben Klasse oder einer verwandten Klasse. Dadurch wird das Lesen mehrerer Nachrichten derselben Klasse effizienter, da Clientanwendungen formularobjekte nach Möglichkeit wiederverwenden können. 
  
Die meisten Formularobjekte verwenden die Nachrichtenklasse, auf die der  _Parameter lpszMessageClass_ verweist, um zu bestimmen, ob sie die nächste Nachricht verarbeiten können. In der Regel kann ein Formular Nachrichten verarbeiten, die zu Klassen gehören, deren Standardklasse eine Unterklasse ist, zusätzlich zu Nachrichten, die zur Standardklasse gehören. Ein Formular kann jedoch andere Faktoren verwenden, um ohne Frage zu bestimmen, ob eine Nachricht behandelt werden kann, z. B. der gesendete oder nicht gesendete Status der nächsten Nachricht. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Geben Sie S_OK und NULL im  _Parameter ppPersistMessage_ zurück, wenn das Formular die Nachrichtenklasse verarbeiten kann. Wenn das Formular ein neues Formular erstellen kann, das die Nachricht verarbeiten kann, die das Formular nicht verarbeiten kann, führen Sie die folgenden Schritte aus: 
  
1. Rufen Sie die Klassenfactory des Formulars auf, um eine Instanz eines neuen Formularobjekts zu erstellen.
    
2. Store diese Instanz im Inhalt des _ppPersistMessage-Zeigerparameters_ ein. 
    
3. Geben Sie S_OK zur�ck.
    
Die Formularanzeige lädt die Nachricht mithilfe der [IPersistMessage::Load-Methode,](ipersistmessage-load.md) die zu dem Objekt gehört, auf das durch  _ppPersistMessage_ verwiesen wird.
  
Wenn weder das Formular noch ein Formular, das Sie erstellen können, die nächste Nachricht verarbeiten können, geben Sie S_FALSE zurück. Im Allgemeinen sollten Formulare diesen Wert jedoch nicht zurückgeben, da er zu leistungsbeeinträchtigungen im Formularviewer führt.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI verwendet die **IMAPIFormAdviseSink::OnActivateNext-Methode,** um die [IMAPIViewContext::ActivateNext-Methode](imapiviewcontext-activatenext.md) zu implementieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

