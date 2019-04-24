---
title: Stornieren einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326404"
---
# <a name="canceling-a-notification"></a>Stornieren einer Benachrichtigung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Um eine Benachrichtigung abzubrechen, rufen die Clients eine **Unadvise** -Methode der Advise-Quelle auf. Das **** Aufrufen von Unadvise ist wichtig, da der Dienstanbieter den Verweis auf Ihre Advise-Senke freigibt. Solange ein Dienstanbieter einen Verweis auf eine Advise-Senke beibehält, kann die Advise-Senke weiterhin [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Anrufe empfangen. Aufgrund der asynchronen Art der Ereignisbenachrichtigung können Clients sogar nach einem erfolgreichen Unadvise-Aufruf benachrichtigt werden **** . Clients müssen den Empfang von Benachrichtigungen jederzeit verarbeiten können. 
  
Da sich die Implementierung von Dienstanbietern unterscheidet, **** können Clients, die nicht Unadvise aufrufen, eine Benachrichtigung abzubrechen, nicht davon ausgehen, wann ein Anbieter ihren Verweis auf die Advise-Senke freigibt. Einige Dienstanbieter veröffentlichen ihre Verweise auf Advise-Senken, wenn Sie Ihre Advise-Quellen freigeben. Einige Dienstanbieter nicht. Solange ein Dienstanbieter einen Verweis auf eine Advise-Senke beibehält, kann diese Advise-Senke weiterhin Benachrichtigungen erhalten. 
  

