---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411764"
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
  
> [in] Eine Bitmaske mit client- oder anbieterdefinierten Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft der nächsten anzuzeigenden Nachricht kopiert werden, die Statusinformationen zur Inhaltstabelle enthält, in der die Nachricht enthalten ist.
    
 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske von **Flags,** die aus der PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der nächsten anzuzeigenden Nachricht kopiert wurden, die den aktuellen Status der Nachricht angibt.
    
 _ppPersistMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die [IPersistMessage-Implementierung](ipersistmessageiunknown.md) für das Formularobjekt, das für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist. Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt zum Anzeigen und Speichern der nächsten Nachricht verwendet werden kann. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.
    
S_FALSE 
  
> Das Formular verarbeiten nicht die Nachrichtenklasse der nächsten Nachricht.
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIFormAdviseSink::OnActivateNext-Methode** auf, um dem Formular zu helfen, zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden kann. Die nächste Nachricht kann eine Nachricht einer beliebigen Klasse sein, aber in der Regel handelt es sich um dieselbe Klasse oder eine verwandte Klasse. Dadurch wird das Lesen mehrerer Nachrichten derselben Klasse effizienter, indem Clientanwendungen die Wiederverwendung von Formularobjekten nach Möglichkeit ermöglichen. 
  
Die meisten Formularobjekte verwenden die Nachrichtenklasse, auf die der  _lpszMessageClass-Parameter_ verweist, um zu bestimmen, ob sie die nächste Nachricht verarbeiten können. In der Regel kann ein Formular Nachrichten verarbeiten, die zu Klassen gehören, deren Standardklasse des Formulars eine Unterklasse ist, zusätzlich zu Nachrichten, die zur Standardklasse gehören. Ein Formular kann jedoch andere Faktoren verwenden, um ohne Frage zu bestimmen, ob eine Nachricht verarbeitet werden kann, z. B. den gesendeten oder nicht gesendeten Status der nächsten Nachricht. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Geben S_OK und NULL im  _ppPersistMessage-Parameter_ zurück, wenn das Formular die Nachrichtenklasse verarbeiten kann. Wenn das Formular ein neues Formular erstellen kann, das die Nachricht verarbeiten kann, die das Formular nicht verarbeiten kann, führen Sie die folgenden Schritte aus: 
  
1. Rufen Sie die Klassen factory des Formulars auf, um eine Instanz eines neuen Formularobjekts zu erstellen.
    
2. Store instanz im Inhalt des _ppPersistMessage-Zeigerparameters._ 
    
3. Geben Sie S_OK zur�ck.
    
Die Formularanzeige wird die Nachricht mithilfe der [IPersistMessage::Load-Methode](ipersistmessage-load.md) laden, die zu dem Objekt gehört, auf das _von ppPersistMessage verwiesen wird._
  
Wenn weder das Formular noch ein Formular, das Sie erstellen können, die nächste Nachricht verarbeiten kann, geben Sie S_FALSE. Im Allgemeinen sollten Formulare diesen Wert jedoch nicht zurückgeben, da dadurch die Leistung in der Formularanzeige verringert wird.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI verwendet die **IMAPIFormAdviseSink::OnActivateNext-Methode,** um die [IMAPIViewContext::ActivateNext-Methode zu](imapiviewcontext-activatenext.md) implementieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

