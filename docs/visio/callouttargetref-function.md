---
title: CALLOUTTARGETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337247"
---
# <a name="callouttargetref-function"></a>CALLOUTTARGETREF Function

Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

CALLOUTTARGETREF ()!
  
### <a name="return-value"></a>Rückgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Bemerkungen

Wenn es sich bei dem Shape nicht um ein Beschriftungs-Shape handelt oder wenn es nicht mit einem Ziel-Shape verknüpft ist, gibt CALLOUTTARGETREF #REF zurück.
  
## <a name="example"></a>Beispiel

CALLOUTTARGETREF ()! Höhe 
  
Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist. 
  

