---
title: Behandeln von Tabelle Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595132"
---
# <a name="handling-table-notification"></a>Behandeln von Tabelle Benachrichtigung

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Client kann als Alternative zum Registrieren direkt mit einer Advise-Quellobjekt, beispielsweise einen Ordner oder ein messaging-Benutzer für Benachrichtigungen auf einem Inhalt registrieren oder Hierarchietabelle. Einträge, Ordner und Nachrichten über eine Inhalt zum Nachverfolgen von Änderungen an-Adresse Buch oder Hierarchietabelle sind einfacher als auch einfacher, als über die einzelnen Objekte. 

Beispielsweise können Sie [IMAPITable::Advise](imapitable-advise.md) für einen Ordner Hierarchietabelle ermitteln können, falls sich ein Unterordner aufrufen. Wenn Sie das Anzeigen von remote-Nachrichten unterstützen, registrieren Sie die Statustabelle auf Aktivität von Anbietern für Transport, und die MAPI-Warteschlange einzuhalten. 
  
Es ist jedoch nicht immer vorzuziehen Tabelle Benachrichtigungen anstelle von Benachrichtigungen Objekt zu verwenden. Überwachen von Änderungen in die Anzahl der Nachrichten in einem Ordner ist ein Beispiel für bei Ihrem Client möglicherweise für Objekt Benachrichtigungen auf einen Ordner und nicht auf einer Tabelle, die durch den Ordner implementiert registriert.
  

