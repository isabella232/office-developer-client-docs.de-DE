---
title: Aufrufen von QueryRows für kleine Tabellen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c38bb0f-de0b-4d70-9f6d-db652445e137
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34975677bedccf3f9111985d371e21d482b45584
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589336"
---
# <a name="calling-queryrows-for-small-tables"></a>Aufrufen von QueryRows für kleine Tabellen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beim Abrufen von Zeilen aus einer kleinen Tabelle rufen Sie [IMAPITable::QueryRows](imapitable-queryrows.md) anstelle der ersten Erstellung einer Einschränkung auf. Erstellen eine Einschränkung beeinträchtigt die Leistung, da der Anbieter muss zuerst erstellen Sie eine Tabelle, die übereinstimmenden Zeilen in der ursprünglichen Tabelle finden und Sie die Zeilen in der neuen Tabelle kopieren. Wenn die Gesamtzahl der Zeilen in der Tabelle weniger als 100 ist, ist es wahrscheinlich effektivere Lesen aller Zeilen und rufen Sie dann [IMAPITable](imapitable-findrow.md) , um die entsprechende Zeile zu finden. Dies ist eine gute Strategie, falls diese Informationen nur gelegentlich erforderlich ist. 
  
Geeigneten Zeitpunkt eine Einschränkung zu verwenden ist, wenn die eingeschränkte oder gefilterte Informationen über einen längeren Zeitraum verwendet oder häufig verwendet werden. Beispielsweise wenn Sie eine Ansicht mit ungelesene Nachrichten immer benötigen, ist eine Beschränkung der richtigen Aufruf verwenden.
  

