---
title: MAPI-Formularschnittstellen
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
# <a name="mapi-form-interfaces"></a>MAPI-Formularschnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert die folgenden Schnittstellen in Bezug auf Formulare.
  
|**Schnittstellenname**|**Beschreibung**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Bearbeitet Formularobjekte und verarbeitet Formularobjektbefehle.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Bestimmt, ob das Formularobjekt die nächste Nachricht verarbeiten kann, und ändert den nächsten oder vorherigen Status des Formularobjekts.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Unterstützt die Installation, Deinstallation und Auflösung von Formularservern für einen bestimmten Formularcontainer.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Unterstützt die Verwendung konfigurierbarer Laufzeitformularserver.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Ermöglicht Clientanwendungen die Arbeit mit Eigenschaften, die für eine Nachrichtenklasse spezifisch sind.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Ermöglicht Clientanwendungen, Informationen zu Formularservern zu erhalten, Formularserver zu aktivieren und Formularserver im Messagingsystem zu installieren.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Wird verwendet, um Nachrichten zu bearbeiten, die Formularobjekten zugeordnet sind.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Benachrichtigt Clientanwendungen, dass ein Ereignis im Formularobjekt aufgetreten ist.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Wird verwendet, um auf die Befehle Next, Previous und Delete im Formularobjekt zu reagieren.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Wird zum Speichern, Initialisieren und Laden von Formularobjekten in und aus dem Nachrichtenspeicher verwendet.  <br/> |
   
Weitere Informationen zu den Methoden der MAPI-Formularschnittstellen finden Sie in der Dokumentation zu diesen Schnittstellen. Sie müssen nicht alle MAPI-Formularschnittstellen implementieren, um ein benutzerdefiniertes Formular zu erstellen. Ein Formular selbst erfordert nur, dass Sie die **Schnittstellen IPersistMessage,** **IMAPIForm** und **IMAPIFormAdviseSink** implementieren. Darüber hinaus ist es auch eine gute Idee, **IMAPIFormFactory** und **IMAPIFormInfo zu implementieren.** **IMAPIFormFactory ist** nützlich für die OLE-Compliance, und **IMAPIFormInfo** ermöglicht gut geschriebenen Clientanwendungen eine bessere Nutzung Ihrer Formulare. 
  
> [!NOTE]
> Genau genommen ist **IMAPIFormAdviseSink** eine optionale Schnittstelle. Es wird jedoch dringend empfohlen, sie auf Ihren Formularservern zu implementieren. Diese Schnittstelle ist entscheidend für die effiziente Interaktion zwischen Messagingclients und Formularservern, insbesondere wenn mehrere Nachrichten der Nachrichtenklasse des Formularservers behandelt werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

