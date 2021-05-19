---
title: Abbrechen einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409762"
---
# <a name="canceling-a-notification"></a>Abbrechen einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Abbrechen einer Benachrichtigung rufen Clients die **Unadvise-Methode** einer Beratenden Quelle auf. Das **Aufrufen von Unadvise** ist wichtig, da der Dienstanbieter seinen Verweis auf Ihre Ratgebersenke veröffentlicht. Solange ein Dienstanbieter einen Verweis auf eine Ratgebersenke verwaltet, kann die Ratgebersenke weiterhin [IMAPIAdviseSink::OnNotify-Anrufe](imapiadvisesink-onnotify.md) empfangen. Aufgrund der asynchronen Art der Ereignisbenachrichtigung können Clients auch nach einem erfolgreichen **Unadvise-Aufruf benachrichtigt** werden. Clients müssen den Empfang von Benachrichtigungen jederzeit verarbeiten können. 
  
Da sich die Implementierungen des Dienstanbieters unterscheiden, können Clients, die **Unadvise** nicht aufrufen, um eine Benachrichtigung abgesagt zu werden, nicht davon ausgehen, wann ein Anbieter seinen Verweis auf seine Ratgebersenke veröffentlicht. Einige Dienstanbieter geben ihre Referenzen frei, um Senken zu beraten, wenn sie ihre Ratgeberquellen veröffentlichen. Einige Dienstanbieter nicht. Solange ein Dienstanbieter einen Verweis auf eine Ratgebersenke verwaltet, kann die Ratgebersenke weiterhin Benachrichtigungen empfangen. 
  

