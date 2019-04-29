---
title: MAPI-Formular Schnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412345"
---
# <a name="mapi-form-interfaces"></a>MAPI-Formular Schnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert die folgenden Schnittstellen im Zusammenhang mit Formularen.
  
|**Schnittstellenname**|**Beschreibung**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Bearbeitet Formularobjekte und verarbeitet Formularobjekt Befehle.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Bestimmt, ob das Form-Objekt die nächste Nachricht verarbeiten und den nächsten oder vorherigen Status des Form-Objekts ändert.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Unterstützt die Installation, Deinstallation und Lösung von Formular Servern für einen bestimmten Formular Container.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Unterstützt die Verwendung von konfigurierbaren Lauf Zeit Formular Servern.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Ermöglicht Clientanwendungen das Arbeiten mit Eigenschaften, die für eine Nachrichtenklasse spezifisch sind.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Ermöglicht es Clientanwendungen, Informationen zu Formular Servern abzurufen, Formularserver zu aktivieren und Formularserver im Messagingsystem zu installieren.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Wird zum Bearbeiten von Nachrichten verwendet, die Formularobjekten zugeordnet sind.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Benachrichtigt Clientanwendungen, dass ein Ereignis im Form-Objekt aufgetreten ist.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Wird verwendet, um auf die Befehle Next, Previous und DELETE im Form-Objekt zu reagieren.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Wird zum Speichern, initialisieren und Laden von Formularobjekten in und aus dem Nachrichtenspeicher verwendet.  <br/> |
   
Weitere Informationen zu den Methoden der MAPI-Formular Schnittstellen finden Sie in der Dokumentation zu diesen Schnittstellen. Sie müssen nicht alle MAPI-Formular Schnittstellen implementieren, um ein benutzerdefiniertes Formular zu erstellen. Ein Formular selbst erfordert nur, dass Sie die **IPersistMessage**-, **IMAPIForm**-und **IMAPIFormAdviseSink** -Schnittstellen implementieren. Darüber hinaus empfiehlt es sich auch, **IMAPIFormFactory** und **IMAPIFormInfo**zu implementieren. **IMAPIFormFactory** ist für die OLE-Kompatibilität hilfreich, und **IMAPIFormInfo** ermöglicht es gut geschriebenen Clientanwendungen, ihre Formulare besser zu verwenden. 
  
> [!NOTE]
> **IMAPIFormAdviseSink** ist eine optionale Schnittstelle. Es wird jedoch dringend empfohlen, dass Sie es in ihren Formular Servern implementieren. Diese Schnittstelle ist für eine effiziente Interaktion zwischen Messagingclients und Formular Servern entscheidend, insbesondere dann, wenn mehrere Nachrichten der Nachrichtenklasse des Formular Servers behandelt werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

