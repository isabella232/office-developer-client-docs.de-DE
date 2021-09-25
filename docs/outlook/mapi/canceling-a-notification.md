---
title: Abbrechen einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0381adadcebca05281353abed78916b994df59e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576534"
---
# <a name="canceling-a-notification"></a>Abbrechen einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um eine Benachrichtigung abzubrechen, rufen Clients die **Unadvise-Methode** einer Empfehlungsquelle auf. Das Aufrufen **von "Unadvise"** ist wichtig, da der Dienstanbieter seinen Verweis auf Ihre Empfehlungssenke freigibt. Solange ein Dienstanbieter einen Verweis auf eine Empfehlungssenke verwaltet, kann die Empfehlungssenke weiterhin [IMAPIAdviseSink::OnNotify-Aufrufe](imapiadvisesink-onnotify.md) empfangen. Aufgrund des asynchronen Charakters der Ereignisbenachrichtigung können Clients sogar nach einem erfolgreichen Aufruf der **Unadvise** benachrichtigt werden. Clients müssen den Empfang von Benachrichtigungen jederzeit verarbeiten können. 
  
Da sich die Implementierungen von Dienstanbietern unterscheiden, können Clients, die **"Unadvise"** nicht aufrufen, um eine Benachrichtigung abzubrechen, nichts davon ausgehen, wann ein Anbieter seinen Verweis auf seine Empfehlungssenke freigibt. Einige Dienstanbieter geben ihre Referenzen frei, um Senken zu empfehlen, wenn sie ihre Empfehlungsquellen freigeben. Bei einigen Dienstanbietern ist dies nicht der Fall. Solange ein Dienstanbieter einen Verweis auf eine Empfehlungssenke aufrechterhält, kann diese Empfehlungssenke weiterhin Benachrichtigungen empfangen. 
  

