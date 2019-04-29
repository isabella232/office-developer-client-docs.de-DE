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
  
Als Alternative zur direkten Registrierung bei einem Advise-Quellobjekt wie einem Ordner oder einem Messagingbenutzer kann ein Client sich für Benachrichtigungen in einer Inhalts-oder Hierarchietabelle registrieren. Das Nachverfolgen von Änderungen an Adressbucheinträgen, Ordnern und Nachrichten über eine Inhalts-oder Hierarchietabelle kann einfacher und geradliniger sein als durch einzelne Objekte. 

Sie können beispielsweise [IMAPITable:: Advise](imapitable-advise.md) für die Hierarchietabelle eines Ordners aufrufen, um zu ermitteln, wann Änderungen an einem der Unterordner vorgenommen werden. Wenn Sie die Anzeige von Remotenachrichten unterstützen, registrieren Sie sich in der Statustabelle, um die Aktivitäten von Transportanbietern und dem MAPI-Spooler zu überwachen. 
  
Es ist jedoch nicht immer vorzuziehen, Tabellen Benachrichtigungen anstelle von Objekt Benachrichtigungen zu verwenden. Das überWachen von Änderungen an der Anzahl von Nachrichten in einem Ordner ist ein Beispiel dafür, wann Ihr Client sich möglicherweise für Objekt Benachrichtigungen in einem Ordner anstatt in einer vom Ordner implementierten Tabelle registrieren muss.
  

