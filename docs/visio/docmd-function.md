---
title: DOCMD-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Führt den identifizierten Befehl aus.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315232"
---
# <a name="docmd-function"></a>DOCMD Function

Führt den identifizierten Befehl aus.
  
## <a name="syntax"></a>Syntax

 **DoCmd** ( _CommandID_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Erforderlich  <br/> |**Number** <br/> | Der auszuführende Befehl.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Eine Liste der Befehle, die mit der DOCMD-Funktion unterstützt werden, finden Sie im Thema "DoCmd/DOCMD-Befehle" in der Microsoft Visio 2013-AutomatisierungsReferenz. 
  
## <a name="example"></a>Beispiel

 `DOCMD (1312)`
  
Bewirkt, dass das Dialogfeld **Shape-Daten** auf der Benutzeroberfläche angezeigt wird. 
  

