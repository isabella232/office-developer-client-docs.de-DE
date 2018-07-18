---
title: Behandeln von Tabelle Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 95ef351e4fe906608319a3e25de8f20a44e23d9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791824"
---
# <a name="handling-table-notification"></a>Behandeln von Tabelle Benachrichtigung

**Betrifft**: Outlook 
  
Ein Client kann als Alternative zum Registrieren direkt mit einer Advise-Quellobjekt, beispielsweise einen Ordner oder ein messaging-Benutzer für Benachrichtigungen auf einem Inhalt registrieren oder Hierarchietabelle. Einträge, Ordner und Nachrichten über eine Inhalt zum Nachverfolgen von Änderungen an-Adresse Buch oder Hierarchietabelle sind einfacher als auch einfacher, als über die einzelnen Objekte. 

Beispielsweise können Sie [IMAPITable::Advise](imapitable-advise.md) für einen Ordner Hierarchietabelle ermitteln können, falls sich ein Unterordner aufrufen. Wenn Sie das Anzeigen von remote-Nachrichten unterstützen, registrieren Sie die Statustabelle auf Aktivität von Anbietern für Transport, und die MAPI-Warteschlange einzuhalten. 
  
Es ist jedoch nicht immer vorzuziehen Tabelle Benachrichtigungen anstelle von Benachrichtigungen Objekt zu verwenden. Überwachen von Änderungen in die Anzahl der Nachrichten in einem Ordner ist ein Beispiel für bei Ihrem Client möglicherweise für Objekt Benachrichtigungen auf einen Ordner und nicht auf einer Tabelle, die durch den Ordner implementiert registriert.
  

