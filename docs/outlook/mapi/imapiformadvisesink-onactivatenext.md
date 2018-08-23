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
ms.openlocfilehash: 7e8fb69e7d25420186d7269943c5d957311e813d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581756"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, ob das Formular die Nachrichtenklasse für die nächste anzuzeigende Meldung verarbeiten kann.
  
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
  
> [in] Ein Zeiger auf die Nachrichtenklasse des nächsten Nachricht.
    
 _ulMessageStatus_
  
> [in] Eine Bitmaske vom Client definiert oder vom Anbieter definiertes Flags, die aus der **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft die nächste Nachricht angezeigt kopiert, bereitstellt, die Statusinformationen bezüglich der Inhaltstabelle, dass die Nachricht enthalten ist. in.
    
 _ulMessageFlags_
  
> [in] Ein Zeiger auf eine Bitmaske aus Flags aus der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft, die an die nächste Nachricht kopiert gibt den aktuellen Status der Nachricht an.
    
 _ppPersistMessage_
  
> [out] Ein Zeiger auf einen Zeiger auf die [IPersistMessage](ipersistmessageiunknown.md) -Implementierung für das Form-Objekt für das neue Formular verwendet wird, wenn ein neues Formular erforderlich ist. Ein Zeiger auf NULL kann zurückgegeben werden, wenn das aktuelle Formularobjekt zum Anzeigen und speichern die nächste Nachricht verwendet werden kann. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Benachrichtigung war erfolgreich, und das Formular kann die nächste Nachricht verarbeiten.
    
S_FALSE 
  
> Das Formular behandelt die Nachrichtenklasse für die nächste Nachricht nicht.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formular Viewer rufen Sie die **IMAPIFormAdviseSink::OnActivateNext** -Methode, mit denen das Formular zu bestimmen, ob die nächste Nachricht in einem Ordner angezeigt werden können. Die nächste Nachricht konnte eine Nachricht einer beliebigen Klasse werden, jedoch ist normalerweise der gleichen Klasse oder einer verknüpften-Klasse. Dadurch wird das Lesen von mehrere Nachrichten von der gleichen Klasse effizienter durch Clientanwendungen Formularobjekte nach Möglichkeit wiederverwenden aktivieren. 
  
Die meisten Formularobjekte werden die Nachrichtenklasse auf das durch den Parameter _LpszMessageClass_ verwenden, um festzustellen, ob sie die nächste Nachricht verarbeiten können. In der Regel kann ein Formular Verarbeitung von Nachrichten, die zu Klassen, von denen Standard-Klasse des Formulars eine Unterklasse, zusätzlich zu Nachrichten gehören, die der Default-Klasse angehören. Ein Formular kann jedoch andere Faktoren verwenden, um ohne Frage zu bestimmen, ob eine Nachricht kann, wie beispielsweise der Status gesendet, der die nächste Nachricht verarbeitet werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Zurückgeben Sie S_OK und NULL in der _PpPersistMessage_ -Parameter, wenn das Formular die Nachrichtenklasse verarbeitet werden kann. Wenn das Formular ein neues Formular, das die Nachricht verarbeitet werden können, die das Formular nicht behandelt wird erstellen kann, gehen Sie folgendermaßen vor: 
  
1. Rufen Sie das Formular Klassenfactory zum Erstellen einer Instanz eines neuen Formulars-Objekts.
    
2. Speichern Sie diese Instanz, in den Inhalt des Parameters Zeiger _PpPersistMessage_ . 
    
3. Geben Sie S_OK zur�ck.
    
Der Formular-Viewer lädt die Nachricht mit der [IPersistMessage::Load](ipersistmessage-load.md) -Methode, die auf das Objekt, auf das _PpPersistMessage_gehört.
  
Wenn weder das Formular noch ein Formular, das Sie erstellen können die nächste Nachricht behandeln, zurückgeben Sie S_FALSE. Allerdings sollte im Allgemeinen Formulare nicht zurückgegeben werden, dass dieser Wert, da dadurch die Leistung im Formular-Viewer verringert.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFormAdviseSink::OnActivateNext** -Methode, um die [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) -Methode zu implementieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[PidTagMessageFlags (kanonische Eigenschaft)](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

