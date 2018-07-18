---
title: CONTAINERSHEETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796734"
---
# <a name="containersheetref-function"></a>CONTAINERSHEETREF Function

Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

CONTAINERSHEETREF (** *Index* ** ** *[, Kategorie]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der auf 1 basierende Index des Containers. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
| _category_ <br/> |Optional  <br/> |**String** <br/> |Die Kategorie des Containers. Weitere Informationen finden Sie unter "Anmerkungen".  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Bemerkungen

Der Index eines Containers wird basierend auf der Z-Reihenfolge der Container von vorne nach hinten berechnet.
  
 *Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, die Shapes kategorisieren. Sie können die Kategorien in der Zelle User.msvShapeCategories im ShapeSheet für ein Shape definieren. Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch ein Semikolon voneinander getrennt. 
  
Wenn das Shape nicht Element eines Containers ist, oder wenn es keinen Container gibt, der sowohl der angegebenen Indexnummer als auch der Kategorie entspricht, gibt CONTAINERSHEETREF #REF! zurück.
  
## <a name="example"></a>Beispiel

CONTAINERSHEETREF(1)!Height 
  
Gibt den Wert in der Zelle Height des Containers zurück, der sich auf der Seite, auf der sich das Shape befindet, am weitesten vorne befindet. 
  

