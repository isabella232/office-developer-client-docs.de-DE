---
title: CALLOUTTARGETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
ms.openlocfilehash: 6213203d951ae972ae923e6b542d6d1cf9d270bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628724"
---
# <a name="callouttargetref-function"></a>CALLOUTTARGETREF Function

Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

CALLOUTTARGETREF()!
  
### <a name="return-value"></a>Rückgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Bemerkungen

Wenn das Shape kein Beschriftungs-Shape ist oder keinem Ziel-Shape zugeordnet ist, gibt CALLOUTTARGETREF #REF zurück.
  
## <a name="example"></a>Beispiel

CALLOUTTARGETREF()! Höhe 
  
Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist. 
  

