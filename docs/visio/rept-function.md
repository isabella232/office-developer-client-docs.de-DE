---
title: REPT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
ms.localizationpriority: medium
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Wiederholt Text so oft wie angegeben.
ms.openlocfilehash: 4a0741fc5ea15540d61d66d16004e5d0db5e381d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559654"
---
# <a name="rept-function"></a>REPT Function

Wiederholt Text so oft wie angegeben. 
  
## <a name="syntax"></a>Syntax

REPT (** *text* **, ** *number_times* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, der wiederholt werden soll.  <br/> |
| _number_times_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine positive Zahl, die angibt, wie oft der Text wiederholt werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn *number_times:* 
  
- Null (0) ist, gibt REPT "" (leeren Text) zurück.
    
- keine Ganzzahl ist, wird es abgeschnitten.
    
## <a name="example"></a>Beispiel

REPT (" \* ", 5) 
  
Gibt \* \* \* \* \* zurück. 
  

