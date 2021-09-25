---
title: DOCMD-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
ms.localizationpriority: medium
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Führt den identifizierten Befehl aus.
ms.openlocfilehash: b6ab817dd437cd844bab4662fbb76f6921cd36a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628451"
---
# <a name="docmd-function"></a>DOCMD Function

Führt den identifizierten Befehl aus.
  
## <a name="syntax"></a>Syntax

 **DOCMD**( _commandID_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Commandid_ <br/> |Erforderlich  <br/> |**Number** <br/> | Der auszuführende Befehl.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Liste der Befehle, die mit der DOCMD-Funktion unterstützt werden, finden Sie im Thema "DoCmd/DOCMD-Befehle" in der Microsoft Visio 2013 Automation Reference. 
  
## <a name="example"></a>Beispiel

 `DOCMD (1312)`
  
Bewirkt, dass das Dialogfeld **Shape-Daten** auf der Benutzeroberfläche angezeigt wird. 
  

