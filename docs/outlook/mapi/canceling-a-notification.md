---
title: Stornieren einer Benachrichtigungs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791379"
---
# <a name="canceling-a-notification"></a>Stornieren einer Benachrichtigungs

  
  
**Betrifft**: Outlook 
  
Um eine Benachrichtigung zu löschen, rufen Clients einer Advise-Datenquelle **Unadvise** -Methode. Aufrufen von **Unadvise** ist wichtig, da dadurch den Dienstanbieter den Verweis auf die Advise-Empfänger freigeben. Als ein Dienstanbieter einen Verweis auf ein Advise-Empfänger verwaltet werden, kann der Advise-Empfänger weiterhin [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Anrufe entgegennehmen. Aufgrund der asynchronen Art der Benachrichtigung, können sogar Clients benachrichtigt werden, auch nach einer erfolgreichen **Unadvise** aufrufen. Clients müssen, können Sie jederzeit den Empfang von Benachrichtigungen behandeln können. 
  
Da Service Provider Implementierungen unterscheiden, können nicht Clients, die nicht aufrufen **Unadvise** um eine Benachrichtigung abzubrechen nichts zu davon ausgehen bei der Freigabe eines Anbieters seinen Verweis auf ihre Advise-Empfänger. Einige Dienstanbieter freigeben ihre Verweise ausschließlich senken, wenn sie ihren Advise-Quellen freigeben zum. Einige Dienstanbieter nicht. Als ein Dienstanbieter einen Verweis auf ein Advise-Empfänger verwaltet werden, kann diese Advise-Empfänger auch weiterhin zum Empfangen von Benachrichtigungen. 
  

