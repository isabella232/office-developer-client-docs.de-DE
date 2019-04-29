---
title: Eigenschaftenbezeichner und-Typen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 39a5c97c-5ac8-47a8-b193-a4b3ba6a02a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: caba60b7059d1c1f8f0440aeb55abb88801fbc9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437217"
---
# <a name="property-identifiers-and-types"></a>Eigenschaftenbezeichner und-Typen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle MAPI-Eigenschaften werden durch Property-Tags dargestellt. Ein Property-Tag ist ein 32-Bit-Ganzzahl ohne Vorzeichen, der den Bezeichner der Eigenschaft in der hochwertigen 16-Bit-Version und den Typ der Eigenschaft in der niedrigen 16-Bit-Reihenfolge enthält. Eigenschaftstags für alle von MAPI definierten Eigenschaften sind in der Headerdatei mapitags. h enthalten.
  
Eigenschaftsbezeichner werden verwendet, um anzugeben, wofür eine Eigenschaft verwendet wird und wer dafür zuständig ist. Eigenschaftsbezeichner werden durch MAPI in Bereiche unterteilt; wo ein Bezeichner in den Range fällt, gibt seine Verwendung und seinen Besitz an. 
  
Eigenschaftstypen werden verwendet, um das Format der Daten der Eigenschaft anzugeben. MAPI definiert alle gültigen Typen. Clients und Dienstanbieter, die neue Eigenschaften erstellen, müssen einen dieser Typen verwenden. Alle Eigenschaftentypen sind in der Headerdatei mapidefs. h enthalten.
  

