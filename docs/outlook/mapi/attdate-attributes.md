---
title: attDate-Attribute
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4c4b58a5391565fd9a50ed0730cf53ed7e9b8af9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580272"
---
# <a name="attdate-attributes"></a>attDate-Attribute

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle MAPI-Eigenschaften, die sich auf Datums- und Uhrzeitangaben beziehen, werden TNEF-Attributen zugeordnet, die das Präfix **"attDate"** aufweisen. Diese werden alle als **DTR-Strukturen** codiert. Die Datums- und Uhrzeitangaben für Anlagenattribute werden auch als **DTR-Strukturen** codiert. 
  
Alle MAPI-Eigenschaften, die sich auf Datums- und Uhrzeitangaben beziehen, werden TNEF-Attributen zugeordnet, die das Präfix **"attDate"** aufweisen. Diese werden alle als **DTR-Strukturen** codiert. Die Datums- und Uhrzeitangaben für Anlagenattribute werden auch als **DTR-Strukturen** codiert. 
  
Eine **DTR-Struktur** ähnelt der **systemtime-Struktur,** die in den Win32-Headerdateien definiert ist. Die **DTR-Struktur** wird im TNEF-Stream als **Sizeof(DTR)-Bytes** codiert, beginnend mit dem ersten Element der Struktur. Die **DTR-Struktur** ist im TNEF definiert. H-Headerdatei. 
  

