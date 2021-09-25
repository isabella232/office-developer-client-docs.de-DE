---
title: Laden einer Nachricht in ein Formular
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4bdbe021-d694-4967-a105-4b24f1eebc44
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e50eb3a88d39d28721d38f4bfa6c06f19da5e59c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579714"
---
# <a name="loading-a-message-into-a-form"></a>Laden einer Nachricht in ein Formular

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um eine vorhandene Nachricht mithilfe eines Formularservers in ein Formular zu laden, verwenden Sie eine der folgenden Strategien.
  
- Rufen Sie [IMAPISession::P repareForm](imapisession-prepareform.md) auf, um ein Token zu erstellen, und dann [IMAPISession::ShowForm,](imapisession-showform.md) um das Formular anzuzeigen. 
    
- Rufen Sie [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md)auf. 
    
Die Verwendung der **Strategie "PrepareForm"** und **"ShowForm"** ist relativ einfach, führt jedoch zu Formularen, die in Bezug auf Ihren Client modal sind. Dies liegt daran, dass der Aufruf von **ShowForm** erst zurückgegeben wird, wenn das Formular beendet wurde. Wenn Sie Formulare asynchron behandeln müssen, verwenden Sie diese Strategie nicht. 
  
Die Verwendung der **LoadForm-Strategie** ist schwieriger, da die Methode mehrere Parameter erfordert. Diese Parameter weisen den Formular-Manager an, den richtigen Formularserver im richtigen Kontext zu starten und die richtige Nachricht anzuzeigen. Wenn der Formularserver bereits ausgeführt wird, lädt der Formular-Manager die Nachricht auf den Formularserver, ohne eine neue Instanz des Formularservers zu starten. 
  
Um anzugeben, welcher Formularserver gestartet werden soll, übergeben Sie die Nachrichtenklasse, die vom Zielserver verarbeitet wird, im Inhalt des _LpszMessageClass-Parameters._ Die entsprechende Nachrichtenklasse kann bestimmt werden, indem die **eigenschaft PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) der zu ladenden Nachricht abgerufen wird. Manchmal gibt es keinen Formularserver für die angegebene Nachrichtenklasse, nur einen Formularserver, der Nachrichten verarbeitet, die zur Oberklasse der Nachricht gehören. Wenn Sie es vorziehen, dass die Nachricht nur von einem Formularserver geladen wird, der speziell nachrichten dieser Klasse verarbeiten soll, legen Sie das flag MAPIFORM_EXACTMATCH im **LoadForm-Aufruf** fest. Weitere Informationen finden Sie unter [MAPI-Nachrichtenklassen.](mapi-message-classes.md)
  
 **LoadForm** erfordert außerdem einen Zeiger auf die Nachrichtenwebsite und den Ansichtskontext des Betrachters sowie den Wert für die **Eigenschaften PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Zielnachricht.
  

