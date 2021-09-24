---
title: Eigenschaftsbezeichner und -typen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f1fefed6006dd90b200b8dfdc4ed4337a40a0186
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550176"
---
# <a name="property-identifiers-and-types"></a>Eigenschaftsbezeichner und -typen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle MAPI-Eigenschaften werden durch Eigenschaftstags dargestellt. Ein Eigenschaftstag ist ein 32-Bit-Ganzzahlwert ohne Vorzeichen, der den Bezeichner der Eigenschaft in der hohen Reihenfolge von 16 Bit und den Typ der Eigenschaft in der niedrigen Reihenfolge von 16 Bit enthält. Eigenschaftstags für alle von MAPI definierten Eigenschaften sind in der Headerdatei mapitags.h enthalten.
  
Eigenschaftsbezeichner werden verwendet, um anzugeben, wofür eine Eigenschaft verwendet wird und wer dafür verantwortlich ist. Eigenschaftsbezeichner werden durch MAPI in Bereiche unterteilt. wenn ein Bezeichner in den Bereich fällt, gibt die Verwendung und den Besitz an. 
  
Eigenschaftstypen werden verwendet, um das Format der Daten der Eigenschaft anzugeben. MAPI definiert alle gültigen Typen. Clients und Dienstanbieter, die neue Eigenschaften erstellen, müssen einen dieser Typen verwenden. Alle Eigenschaftstypen sind in der Headerdatei mapidefs.h enthalten.
  

