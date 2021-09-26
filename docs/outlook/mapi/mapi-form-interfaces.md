---
title: MAPI-Formularschnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b314e9c3d0e8ffd82a94ae981b259cb3b845254c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610321"
---
# <a name="mapi-form-interfaces"></a>MAPI-Formularschnittstellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI definiert die folgenden Schnittstellen im Zusammenhang mit Formularen.
  
|**Schnittstellenname**|**Beschreibung**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Bearbeitet Formularobjekte und verarbeitet Formularobjektbefehle.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Bestimmt, ob das Formularobjekt die nächste Nachricht verarbeiten kann, und ändert den nächsten oder vorherigen Status des Formularobjekts.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Unterstützt die Installation, Deinstallation und Auflösung von Formularservern für einen bestimmten Formularcontainer.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Unterstützt die Verwendung konfigurierbarer Laufzeitformularserver.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Ermöglicht Clientanwendungen das Arbeiten mit Eigenschaften, die für eine Nachrichtenklasse spezifisch sind.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Ermöglicht Clientanwendungen das Abrufen von Informationen zu Formularservern, das Aktivieren von Formularservern und das Installieren von Formularservern im Messagingsystem.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Wird zum Bearbeiten von Nachrichten verwendet, die Formularobjekten zugeordnet sind.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Benachrichtigt Clientanwendungen, dass ein Ereignis im Formularobjekt aufgetreten ist.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Wird verwendet, um auf die Befehle Weiter, Zurück und Löschen im Formularobjekt zu antworten.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Wird zum Speichern, Initialisieren und Laden von Formularobjekten in und aus dem Nachrichtenspeicher verwendet.  <br/> |
   
Weitere Informationen zu den Methoden der MAPI-Formularschnittstellen finden Sie in der Dokumentation zu diesen Schnittstellen. Sie müssen nicht alle MAPI-Formularschnittstellen implementieren, um ein benutzerdefiniertes Formular zu erstellen. Ein Formular selbst erfordert nur, dass Sie die **IPersistMessage-,** **IMAPIForm-** und **IMAPIFormAdviseSink-Schnittstellen** implementieren. Darüber hinaus empfiehlt es sich auch, **IMAPIFormFactory** und **IMAPIFormInfo** zu implementieren. **IMAPIFormFactory** ist nützlich für die OLE-Compliance, und **IMAPIFormInfo** ermöglicht gut geschriebenen Clientanwendungen eine bessere Nutzung Ihrer Formulare. 
  
> [!NOTE]
> Genau genommen ist **IMAPIFormAdviseSink** eine optionale Schnittstelle. Es wird jedoch dringend empfohlen, sie auf Den Formularservern zu implementieren. Diese Schnittstelle ist für eine effiziente Interaktion zwischen Messagingclients und Formularservern wichtig, insbesondere, wenn mehrere Nachrichten der Nachrichtenklasse Ihres Formularservers bearbeitet werden. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Formulare](mapi-forms.md)

