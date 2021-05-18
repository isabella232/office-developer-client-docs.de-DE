---
title: attDate-Attribute
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408278"
---
# <a name="attdate-attributes"></a>attDate-Attribute

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle MAPI-Eigenschaften in Bezug auf Datums- und Zeitangaben werden TNEF-Attributen zugeordnet, die das **AttDate-Präfix** aufweisen. Diese werden alle als **DTR-Strukturen** codiert. Die Datums- und Zeitangaben für Anlagenattribute werden ebenfalls als **DTR-Strukturen** codiert. 
  
Alle MAPI-Eigenschaften in Bezug auf Datums- und Zeitangaben werden TNEF-Attributen zugeordnet, die das **AttDate-Präfix** aufweisen. Diese werden alle als **DTR-Strukturen** codiert. Die Datums- und Zeitangaben für Anlagenattribute werden ebenfalls als **DTR-Strukturen** codiert. 
  
Eine **DTR-Struktur** ähnelt der **SYSTEMTIME-Struktur,** die in den Win32-Headerdateien definiert ist. Die **DTR-Struktur** wird im TNEF-Stream als **Sizeof(DTR)-Bytes** codiert, beginnend mit dem ersten Element der Struktur. Die **DTR-Struktur** ist im TNEF definiert. H-Headerdatei. 
  

