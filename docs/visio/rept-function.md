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
description: Wiederholt Text so oft wie angegeben.
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412079"
---
# <a name="rept-function"></a>REPT Function

Wiederholt Text so oft wie angegeben. 
  
## <a name="syntax"></a>Syntax

REPT (* * *Text* * *, * * *Multiplikator* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Text, der wiederholt werden soll.  <br/> |
| _Multiplikator_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine positive Zahl, die angibt, wie oft der Text wiederholt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *Multiplikator* ist: 
  
- Null (0) ist, gibt REPT "" (leeren Text) zurück.
    
- keine Ganzzahl ist, wird es abgeschnitten.
    
## <a name="example"></a>Beispiel

REPT ("\*", 5) 
  
Gibt \* \* \*zurück \*. \* 
  

