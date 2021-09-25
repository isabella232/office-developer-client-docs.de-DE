---
title: Behandeln von Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 874f5954ad24c2714ba06e0050f3bb00b6ef160c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604964"
---
# <a name="handling-table-notification"></a>Behandeln von Tabellenbenachrichtigungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Als Alternative zur direkten Registrierung bei einem Empfehlungsquellobjekt, z. B. einem Ordner oder einem Messaging-Benutzer, kann sich ein Client für Benachrichtigungen in einer Inhalts- oder Hierarchietabelle registrieren. Das Nachverfolgen von Änderungen an Adressbucheinträgen, Ordnern und Nachrichten über einen Inhalt oder eine Hierarchietabelle kann einfacher und einfacher als durch einzelne Objekte sein. 

Sie können z. B. [IMAPITable::Advise](imapitable-advise.md) in der Hierarchietabelle eines Ordners aufrufen, um zu ermitteln, wann Änderungen an einem seiner Unterordner auftreten. Wenn Sie die Anzeige von Remotenachrichten unterstützen, registrieren Sie sich bei der Statustabelle, um aktivitäten von Transportanbietern und dem MAPI-Spooler zu beobachten. 
  
Es ist jedoch nicht immer vorzuziehen, Tabellenbenachrichtigungen anstelle von Objektbenachrichtigungen zu verwenden. Das Überwachen von Änderungen an der Anzahl von Nachrichten in einem Ordner ist ein Beispiel dafür, wann Ihr Client sich möglicherweise für Objektbenachrichtigungen in einem Ordner und nicht für eine vom Ordner implementierte Tabelle registrieren muss.
  

