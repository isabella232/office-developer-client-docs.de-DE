---
title: Abrufen und Festlegen mehrerer Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 88c3e0bdb3cc6660e35faf62c5bb63ec2f6352bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590372"
---
# <a name="getting-and-setting-multiple-properties"></a>Abrufen und Festlegen mehrerer Eigenschaften

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Durch Abrufen und Festlegen von so viele Eigenschaften wie möglich mit der geringsten Anzahl Anrufe, remote Aktivität Falle wird und mit jeder Eigenschaft Verwaltungsaufwand reduziert. Zwar Dienstanbieter versuchen, vor der Durchführung eines Remoteprozeduraufrufs für abrufen oder Ändern von Eigenschaften erfasst werden sollen, können Sie Maßnahme optimieren, indem Sie mehrere Eigenschaften zunächst anfordern.
  
Beispielsweise wenn Sie routing Listen, die mit benannten Eigenschaften von bestimmten Eigenschaftensätze zukünftige Empfänger beschreiben entwickelt, verarbeitet alle Empfänger mit zwei Anrufe entgegennehmen. Verwenden Sie durch Aufrufen von [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , um die Bezeichner für alle den Empfängereigenschaften und den anderen Anruf an [IMAPIProp::GetProps](imapiprop-getprops.md) zum Abrufen aller Werte abzurufen. Die Alternative, tätigen eines Anrufs auf **GetIDsFromNames** gefolgt von einem Aufruf von **GetProps** für jeden Empfänger ist viel weniger effizient. 
  

