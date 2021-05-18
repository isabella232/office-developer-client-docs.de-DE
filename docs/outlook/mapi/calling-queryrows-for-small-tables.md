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
ms.openlocfilehash: 8b38dcc485e75f94ccf4f4c3c8c9a57d314465a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404176"
---
# <a name="calling-queryrows-for-small-tables"></a>Aufrufen von QueryRows für kleine Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Rufen Sie beim Abrufen von Zeilen aus einer kleinen Tabelle [IMAPITable::QueryRows](imapitable-queryrows.md) auf, anstatt zuerst eine Einschränkung zu erstellen. Das Erstellen einer Einschränkung wirkt sich auf die Leistung aus, da der Anbieter zunächst eine Tabelle erstellen, die übereinstimmenden Zeilen in der ursprünglichen Tabelle suchen und dann die Zeilen in die neue Tabelle kopieren muss. Wenn die Gesamtzahl der Zeilen in der Tabelle kleiner als 100 ist, ist es wahrscheinlich effektiver, alle Zeilen zu lesen und [dann IMAPITable::FindRow](imapitable-findrow.md) auf, um die entsprechende Zeile zu finden. Dies ist eine besonders gute Strategie, wenn diese Informationen nur gelegentlich benötigt werden. 
  
Der richtige Zeitpunkt für die Verwendung einer Einschränkung ist, wenn die eingeschränkten oder gefilterten Informationen über einen längeren Zeitraum oder häufig verwendet werden. Wenn Sie beispielsweise immer eine Ansicht mit ungelesenen Nachrichten benötigen, ist eine Einschränkung der richtige Aufruf.
  

