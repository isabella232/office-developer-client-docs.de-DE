---
title: Laden eine Nachricht in ein Formular
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e65311187ba96abde31a4779ebba371b3d02084
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576498"
---
# <a name="loading-a-message-into-a-form"></a>Laden eine Nachricht in ein Formular

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Um eine vorhandene Nachricht in einem Formular mit einem Formular Server zu laden, verwenden Sie eine der folgenden Strategien.
  
- Rufen Sie [IMAPISession::PrepareForm](imapisession-prepareform.md) , um ein Token zu erstellen, und klicken Sie dann [IMAPISession::ShowForm](imapisession-showform.md) um das Formular anzuzeigen. 
    
- Rufen Sie [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md). 
    
Verwenden der Strategie **PrepareForm** und **ShowForm aus** relativ einfach ist, aber es führt zu Formularen, die in Bezug auf Ihrem Client modal sind. Dies ist, da der Anruf an **ShowForm aus** , bis das Formular beendet wurde nicht zurückgibt. Wenn Sie Formulare asynchron verarbeiten müssen, verwenden Sie diese Strategie nicht. 
  
Verwenden der **LoadForm** Strategie ist schwieriger, da die Methode mehrere Parameter erforderlich sind. Diese Parameter weisen den Formular-Manager, starten Sie den Server ordnungsgemäße Formular im richtigen Kontext und die richtige Meldung angezeigt. Wenn der Formular Server bereits ausgeführt wird, lädt der Formular-Manager die Nachricht in dem Formular Server ohne eine neue Instanz des Formulars Servers starten. 
  
Welche Formular Server zu starten, und übergeben Sie die Nachrichtenklasse angeben, die von dem Zielserver in den Inhalt des Parameters _LpszMessageClass_ behandelt werden. Die entsprechende Nachrichtenklasse kann ermittelt werden, durch die Eigenschaft **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der Nachricht zu ladenden abrufen. In einigen Fällen ist kein Formular Server für die angegebene Nachrichtenklasse nur Formular von einem Server, die Nachrichten, die an die Nachricht zur übergeordneten Klasse gehören behandelt. Wenn Sie, dass die Nachricht nur von einem Formular-Server zum Verarbeiten von Nachrichten dieser Klasse speziell dafür vorgesehen geladen werden möchten, legen Sie das MAPIFORM_EXACTMATCH-Flag in den Anruf **LoadForm** . Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).
  
 **LoadForm** erfordert auch einen Zeiger auf Ihre Viewer Nachricht Website und Ansichtskontext und den Wert für die Zielnachricht **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) Eigenschaften.
  

