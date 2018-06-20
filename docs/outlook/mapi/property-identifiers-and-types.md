---
title: Eigenschaftenbezeichner und Typen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f31162e669af6efaf9e935c7c400d105c1321c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795314"
---
# <a name="property-identifiers-and-types"></a>Eigenschaftenbezeichner und Typen

  
  
**Betrifft**: Outlook 
  
Alle MAPI-Eigenschaften werden durch Eigenschaftentags dargestellt. Ein Eigenschaftentag ist ein 32-Bit-Ganzzahl ohne Vorzeichen-Wert, der Eigenschaftenbezeichner in der besonders enthält, bestellen 16 Bit und den Typ der Eigenschaft in den niedrigen bestellen 16 Bit. Eigenschaftentags für alle von MAPI definierten Eigenschaften sind in der Headerdatei mapitags.h enthalten.
  
Eigenschaftenbezeichner werden verwendet, um anzugeben, was für eine Eigenschaft verwendet wird, und wer dafür verantwortlich ist. Eigenschaftenbezeichner sind MAPI in Bereiche unterteilt; Gibt an, bei denen ein Bezeichner des Bereichs liegt, seine Verwendung und den Besitz. 
  
Eigenschaftentypen werden verwendet, um das Format für die Eigenschaft Daten anzugeben. MAPI definiert alle gültigen Typen. Clients und Erstellen neuer Eigenschaften Dienstanbieter müssen eine der folgenden Typen verwenden. Alle die Eigenschaftentypen sind in der Headerdatei mapidefs.h enthalten.
  

