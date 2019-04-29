---
title: Laden einer Nachricht in ein Formular
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: afecd3b334dd2cf7b2953916872982e6459a8434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412415"
---
# <a name="loading-a-message-into-a-form"></a>Laden einer Nachricht in ein Formular

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie eine vorhandene Nachricht mithilfe eines Formular Servers in ein Formular laden möchten, verwenden Sie eine der folgenden Strategien.
  
- Rufen Sie [IMAPISession::P repareform](imapisession-prepareform.md) , um ein Token zu erstellen, und klicken Sie dann auf [IMAPISession:: ShowForm](imapisession-showform.md) , um das Formular anzuzeigen. 
    
- Rufen Sie [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md)auf. 
    
Die Verwendung der **PrepareForm** -und **ShowForm** -Strategie ist vergleichsweise einfach, führt jedoch zu Formularen, die in Bezug auf Ihren Client Modal sind. Der Grund ist, dass der Aufruf von **ShowForm** erst zurückgegeben wird, wenn das Formular beendet wurde. Wenn Sie Formulare asynchron behandeln müssen, verwenden Sie diese Strategie nicht. 
  
Die Verwendung der **LoadForm** -Strategie ist schwieriger, da die Methode mehrere Parameter erfordert. Diese Parameter weisen den Formular-Manager an, den richtigen Formularserver im richtigen Kontext zu starten und die entsprechende Meldung anzuzeigen. Wenn der Formularserver bereits aktiv ist, wird die Nachricht vom Formular-Manager in den Formularserver geladen, ohne eine neue Instanz des Formular Servers zu starten. 
  
Um anzugeben, welcher Formularserver gestartet werden soll, übergeben Sie die vom Zielserver verarbeitete Nachrichtenklasse im Inhalt des _lpszMessageClass_ -Parameters. Die entsprechende Nachrichtenklasse kann ermittelt werden, indem die **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft der zu ladenden Nachricht abgerufen wird. Manchmal gibt es keinen Formularserver für die angegebene Nachrichtenklasse, sondern nur einen Formularserver, der Nachrichten verarbeitet, die zur Oberklasse der Nachricht gehören. Wenn Sie es vorziehen, die Nachricht nur von einem Formularserver zu laden, der speziell für die Verarbeitung von Nachrichten dieser Klasse vorgesehen ist, legen Sie das MAPIFORM_EXACTMATCH-Flag im **LoadForm** -Aufruf fest. Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).
  
 **LoadForm** erfordert auch einen Zeiger auf die Nachrichtenwebsite und den Ansichtskontext des Viewers und den Wert für die **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Zielnachricht. Eigenschaften.
  

