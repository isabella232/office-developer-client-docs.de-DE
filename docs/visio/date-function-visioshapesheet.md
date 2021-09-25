---
title: DATE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
ms.localizationpriority: medium
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Gibt das Datum zurück, das durch Jahr, Monat und Tag dargestellt wird, das gemäß der kurzen Datumsformatvorlage in der regionalen Einstellungen des Systems formatiert ist. Die Werte für Jahr, Monat und Tag spiegeln den gregorianischen Kalender wider.
ms.openlocfilehash: 820329bbe9283cae540625d4232d4095c6a1a530
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577906"
---
# <a name="date-function-visioshapesheet"></a>DATE-Funktion (VisioShapeSheet)

Gibt das Datum zurück, das durch *Jahr, Monat* und *Tag* dargestellt wird, das gemäß der kurzen Datumsformatvorlage in der regionalen Einstellungen des Systems formatiert ist. Die Werte für  *Jahr,* *Monat*  und  *Tag*  spiegeln den gregorianischen Kalender wider. 
  
## <a name="syntax"></a>Syntax

DATE(** *year* **, ** *month* **, ** *day* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Das Jahr.  <br/> |
| _Monat_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Monat.  <br/> |
| _day_ <br/> |Erforderlich  <br/> |**Integer** <br/> |Der Tag.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

DATE(1999,6,7)
  
Gibt den Wert zurück, der 07.06.99 darstellt.
  
## <a name="example-2"></a>Beispiel 2

DATE(1999,6,7) + 4 t.
  
Gibt den Wert zurück, der 11.06.99 darstellt.
  
## <a name="example-3"></a>Beispiel 3

FORMAT(DATE(1999,10,14),"C")
  
Gibt den Wert zurück, der Dienstag, 14. Oktober 1999 darstellt.
  

