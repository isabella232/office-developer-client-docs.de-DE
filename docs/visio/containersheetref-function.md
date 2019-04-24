---
title: CONTAINERSHEETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318984"
---
# <a name="containersheetref-function"></a>CONTAINERSHEETREF Function

Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

CONTAINERSHEETREF (* * *Index* * * * * * *[, Category]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der auf 1 basierende Index des Containers. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
| _Kategorie_ <br/> |Optional  <br/> |**String** <br/> |Die Kategorie des Containers. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
   
### <a name="return-value"></a>Rückgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Bemerkungen

Der Index eines Containers wird basierend auf der Z-Reihenfolge der Container von vorne nach hinten berechnet.
  
 *Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, um Shapes zu kategorisieren. Kategorien können in der Zelle User.msvShapeCategories im ShapeSheet eines Shapes definiert werden. Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch Semikolons trennen. 
  
Wenn das Shape nicht Element eines Containers ist, oder wenn es keinen Container gibt, der sowohl der angegebenen Indexnummer als auch der Kategorie entspricht, gibt CONTAINERSHEETREF #REF! zurück.
  
## <a name="example"></a>Beispiel

CONTAINERSHEETREF (1)! Höhe 
  
Gibt den Wert in der Zelle Height des Containers zurück, der sich auf der Seite, auf der sich das Shape befindet, am weitesten vorne befindet. 
  

