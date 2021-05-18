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
  
Verwenden Sie eine der folgenden Strategien, um eine vorhandene Nachricht mithilfe eines Formularservers in ein Formular zu laden.
  
- Rufen [Sie IMAPISession::P repareForm](imapisession-prepareform.md) auf, um ein Token zu erstellen, und dann [IMAPISession::ShowForm](imapisession-showform.md) zum Anzeigen des Formulars. 
    
- Rufen [Sie IMAPIFormMgr::LoadForm auf.](imapiformmgr-loadform.md) 
    
Die **Verwendung der PrepareForm-** und **ShowForm-Strategie** ist vergleichsweise einfach, führt jedoch zu modalen Formularen im Hinblick auf Ihren Client. Der Grund dafür ist, dass der Aufruf von **ShowForm** erst zurückt, wenn das Formular beendet wurde. Wenn Sie Formulare asynchron behandeln müssen, verwenden Sie diese Strategie nicht. 
  
Die **Verwendung der LoadForm-Strategie** ist schwieriger, da die Methode mehrere Parameter erfordert. Mit diesen Parametern wird der Formular-Manager angewiesen, den richtigen Formularserver im richtigen Kontext zu starten und die richtige Nachricht anzeigen zu können. Wenn der Formularserver bereits ausgeführt wird, lädt der Formular-Manager die Nachricht auf den Formularserver, ohne eine neue Instanz des Formularservers zu starten. 
  
Um anzugeben, welcher Formularserver gestartet werden soll, übergeben Sie die nachrichtenklasse, die vom Zielserver verarbeitet wird, im Inhalt des _lpszMessageClass-Parameters._ Die entsprechende Nachrichtenklasse kann durch Abrufen der **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft der zu ladenden Nachricht bestimmt werden. Manchmal gibt es keinen Formularserver für die angegebene Nachrichtenklasse, sondern nur einen Formularserver, der Nachrichten verarbeitet, die zur Überklasse der Nachricht gehören. Wenn Sie es vorziehen, dass die Nachricht nur von einem Formularserver geladen wird, der speziell für die Verarbeitung von Nachrichten dieser Klasse gedacht ist, legen Sie das MAPIFORM_EXACTMATCH im **LoadForm-Aufruf** fest. Weitere Informationen finden Sie unter [MAPI Message Classes](mapi-message-classes.md).
  
 **LoadForm** erfordert außerdem einen Zeiger auf die Nachrichtenwebsite und den Ansichtskontext des Betrachters sowie den Wert für die **Eigenschaften PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) und **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) der Zielnachricht.
  

