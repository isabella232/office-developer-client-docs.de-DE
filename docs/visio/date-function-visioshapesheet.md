---
title: DATE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Gibt das Durch Jahr, Monat und Tag dargestellte Datum zurück, das gemäß der kurzen Datumsart im regionalen Format des Systems Einstellungen. Die Werte für Jahr, Monat und Tag spiegeln den gregorianischen Kalender wider.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360333"
---
# <a name="date-function-visioshapesheet"></a>DATE-Funktion (VisioShapeSheet)

Gibt das Durch Jahr, Monat  und Tag dargestellte Datum *zurück,* das gemäß der kurzen Datumsart im regionalen Format des Systems Einstellungen. Die Werte für  *Jahr,* *Monat*  und  *Tag spiegeln*  den gregorianischen Kalender wider. 
  
## <a name="syntax"></a>Syntax

DATE(** *Jahr* **, ** *Monat* **, ** *Tag* ** ) 
  
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
  

