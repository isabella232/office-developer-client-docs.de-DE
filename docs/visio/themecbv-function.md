---
title: THEMECBV Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die als Argument übergebene Farbe (Zahl) durch den angegebenen Farbton oder Schattierungswert geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429138"
---
# <a name="themecbv-function"></a>THEMECBV Function

Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die als Argument übergebene Farbe (Zahl) durch den angegebenen Farbton oder Schattierungswert geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **THEMECBV**( _color_,  _gradient_stop_number_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine Zahl, die einen Index in der Farbpalette des Dokuments darstellt.  <br/> |
| _gradient_stop_number_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Farbverlaufsstopp (Farbton oder Schatten), der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist, das auf die Farbe angewendet werden soll.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>Hinweise

> [!NOTE]
> Die THEMECBV-Funktion führt nichts zu der Farbe aus, die als Argument übergeben wird, wenn der dem Shape zugewiesene QuickStyle keinen Farbverlauf hat. 
  
Die Farbverlaufseinstellungen in einem Design sind eine Reihe von nummerierten Farbverlaufsstopps, die einer "Auflichtung" (Farbton) oder "Abdunklerung" (Schattierung) entsprechen. Diese Schattierungen und Farbtons werden auf eine Basisfarbe angewendet, um einen Farbverlaufseffekt zu erzeugen.
  
Die **THEMECBV-Funktion** übernimmt eine Farbeingabe und gibt die Farbe aus, nachdem sie durch den Farbton oder schatten des angegebenen Farbverlaufsstopps geändert wurde. Die Farbtons und Schattierungen stammen aus der Designdefinition, wenn die aktuelle Schnellformatvorlage eine Farbverlaufsfüllung enthält. Wenn die aktive Schnellformatvorlage keine Farbverlaufsfüllung angibt oder die Form auf Kein Design festgelegt ist, gibt diese Formel einfach die Farbe zurück, die für das erste Argument übergeben wurde. 
  
## <a name="example"></a>Beispiel

 `THEMECBV(FillForegnd, 5)`
  
Gibt die Farbe zurück, die durch Anwenden des Farbtons oder der Schattierung im fünften Farbverlaufsstopp des Farbverlaufs auf die in der **FillForegnd-Zelle** angegebene Farbe erstellt wurde. 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Gibt einen Schattierungs- oder Farbton von Rot zurück, der durch Anwenden des zweiten Farbverlaufsstopps auf eine Basisfarbe rot erstellt wurde.
  

