---
title: REPT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Wiederholt den Text eine angegebene Anzahl von Malen.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797874"
---
# <a name="rept-function"></a>REPT Function

Wiederholt den Text eine angegebene Anzahl von Malen. 
  
## <a name="syntax"></a>Syntax

REPT (** *Text* **, ** *Zahl_Wiederholungen* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, der wiederholt werden soll.  <br/> |
| _Zahl_Wiederholungen_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Eine positive Zahl, die angibt, wie oft der Text wiederholt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *number_times:* 
  
- Null (0) ist, gibt REPT "" (leeren Text) zurück.
    
- keine Ganzzahl ist, wird es abgeschnitten.
    
## <a name="example"></a>Beispiel

REPT ("\*", 5) 
  
Gibt \* \* \* \* \*. 
  

