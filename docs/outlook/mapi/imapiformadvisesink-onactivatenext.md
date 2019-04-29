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
  
Gibt an, ob das Formular die Nachrichtenklasse der nächsten anzuzeigende Nachricht behandeln kann.
  
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
  
> in Ein Zeiger auf die Nachrichtenklasse der nächsten Nachricht.
    
 _ulMessageStatus_
  
> in Eine Bitmaske von Client definierten oder Anbieter definierten Flags, die von der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der nächsten anzuzeigende Nachricht kopiert werden und Status Informationen zur Inhaltstabelle bereitstellen, die die Nachricht enthält. in.
    
 _ulMessageFlags_
  
> in Ein Zeiger auf eine Bitmaske von Flags, die von der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft der nächsten anzuzeigende Nachricht kopiert und den aktuellen Status der Nachricht angibt.
    
 _ppPersistMessage_
  
> Out Ein Zeiger auf einen Zeiger auf die [IPersistMessage](ipersistmessageiunknown.md) -Implementierung für das Form-Objekt, das für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist. Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt verwendet werden kann, um die nächste Nachricht anzuzeigen und zu speichern. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.
    
S_FALSE 
  
> Das Formular verarbeitet die Nachrichtenklasse der nächsten Nachricht nicht.
    
## <a name="remarks"></a>Bemerkungen

Formular Betrachter rufen die **IMAPIFormAdviseSink:: OnActivateNext** -Methode auf, um zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden kann. Bei der nächsten Nachricht kann es sich um eine beliebige Klasse handeln, aber in der Regel handelt es sich um eine Klasse oder eine zugehörige Klasse. Dadurch wird der Prozess des Lesens mehrerer Nachrichten derselben Klasse effizienter, indem Clientanwendungen nach Möglichkeit die Wiederverwendung von Formularobjekten ermöglichen. 
  
Die meisten Form-Objekte verwenden die Nachrichtenklasse, auf die durch den _lpszMessageClass_ -Parameter verwiesen wird, um zu bestimmen, ob Sie die nächste Nachricht verarbeiten können. In der Regel kann ein Formular Nachrichten verarbeiten, die zu Klassen gehören, deren Standardklasse eine Unterklasse ist, zusätzlich zu Nachrichten, die zur Standardklasse gehören. Ein Formular kann jedoch andere Faktoren verwenden, um zu bestimmen, ob eine Nachricht verarbeitet werden kann, beispielsweise den Status "gesendet" oder "nicht gesendet" der nächsten Nachricht. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Geben Sie S_OK und NULL im _ppPersistMessage_ -Parameter zurück, wenn das Formular die Nachrichtenklasse verarbeiten kann. Führen Sie die folgenden Schritte aus, wenn das Formular ein neues Formular erstellen kann, das die Nachricht verarbeiten kann, die vom Formular nicht verarbeitet werden konnte: 
  
1. Rufen Sie die Klassen Factory des Formulars auf, um eine Instanz eines neuen Form-Objekts zu erstellen.
    
2. Speichern Sie diese Instanz im Inhalt des _ppPersistMessage_ -Zeiger-Parameters. 
    
3. Geben Sie S_OK zur�ck.
    
Der Formular-Viewer lädt die Nachricht mithilfe der [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode, die zu dem Objekt gehört, auf das durch _ppPersistMessage_verwiesen wird.
  
Wenn weder das Formular noch ein Formular, das Sie erstellen können, die nächste Nachricht verarbeiten kann, geben Sie S_FALSE zurück. Im Allgemeinen sollten Formulare diesen Wert jedoch nicht zurückgeben, da dadurch die Leistung im Formular Betrachter vermindert wird.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CMyMAPIFormViewer:: ActivateNext  <br/> |MFCMAPI verwendet die **IMAPIFormAdviseSink:: OnActivateNext** -Methode, um die [IMAPIViewContext:: ActivateNext](imapiviewcontext-activatenext.md) -Methode zu implementieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[Kanonische PidTagMessageFlags-Eigenschaft](pidtagmessageflags-canonical-property.md)
  
[Kanonische Pidtagmessagestatus (-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

