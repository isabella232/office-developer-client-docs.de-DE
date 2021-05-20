---
title: Behandeln von Tabellenbenachrichtigungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435894"
---
# <a name="handling-table-notification"></a>Behandeln von Tabellenbenachrichtigungen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Als Alternative zur direkten Registrierung bei einem Advise-Quellobjekt, z. B. einem Ordner oder einem Messagingbenutzer, kann sich ein Client für Benachrichtigungen in einer Inhalts- oder Hierarchietabelle registrieren. Das Nachverfolgen von Änderungen an Adressbucheinträgen, Ordnern und Nachrichten über einen Inhalt oder eine Hierarchietabelle kann einfacher und einfacher sein als durch einzelne Objekte. 

Sie können beispielsweise [IMAPITable::Advise](imapitable-advise.md) in der Hierarchietabelle eines Ordners aufrufen, um zu ermitteln, wann Änderungen an einem der Unterordner vorgenommen werden. Wenn Sie die Anzeige von Remotenachrichten unterstützen, registrieren Sie sich bei der Statustabelle, um Aktivitäten von Transportanbietern und dem MAPI-Spooler zu beobachten. 
  
Es ist jedoch nicht immer vorzuziehen, Tabellenbenachrichtigungen anstelle von Objektbenachrichtigungen zu verwenden. Die Überwachung von Änderungen an der Anzahl der Nachrichten in einem Ordner ist ein Beispiel dafür, wann Ihr Client möglicherweise für Objektbenachrichtigungen in einem Ordner und nicht in einer vom Ordner implementierten Tabelle registrieren muss.
  

