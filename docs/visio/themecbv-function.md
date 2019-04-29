---
title: THEMECBV Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die Farbe (Zahl), die als Argument übergeben wurde, durch den angegebenen Farbton oder Farbton geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429138"
---
# <a name="themecbv-function"></a>THEMECBV Function

Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die Farbe (Zahl), die als Argument übergeben wurde, durch den angegebenen Farbton oder Farbton geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **THEMECBV** ( _Farbe_, _gradient_stop_number_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine Zahl, die einen Index in der Farbpalette des Dokuments darstellt.  <br/> |
| _gradient_stop_number_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Farbverlaufsstopp (Farbton oder Schattierung), der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist und auf die Farbe angewendet werden soll.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>Bemerkungen

> [!NOTE]
> Die THEMECBV-Funktion bewirkt keine Farbe, die als Argument übergeben wird, wenn die QuickStyle, die dem Shape zugewiesen ist, keinen Farbverlauf aufweist. 
  
Die Farbverlaufseinstellungen in einem Design sind eine Reihe von nummerierten Farbverlaufs Unterbrechungen, die einer "Aufhellung" (Tönung) oder "Verdunkelung" (Farbton) entsprechen. Diese Schattierungen und Farbtöne werden auf eine Grundfarbe angewendet, um einen Farbverlauf zu erstellen.
  
Die **THEMECBV** -Funktion verwendet eine Farb Eingabe und gibt die Farbe aus, nachdem Sie durch den Farbton oder die Schattierung des angegebenen Farbverlaufsstopps geändert wurde. Die Farbtöne und Schattierungen stammen aus der Definition des Designs, wenn die aktuelle Schnellformatvorlage eine graduelle Füllung enthält. Wenn die aktive Schnellformatvorlage keine Farbverlaufsfüllung angibt oder die Form auf kein Design festgelegt ist, gibt diese Formel einfach die Farbe zurück, die für das erste Argument übergeben wurde. 
  
## <a name="example"></a>Beispiel

 `THEMECBV(FillForegnd, 5)`
  
Gibt die Farbe zurück, die durch Anwenden des Farbtons oder der Schattierung im fünften Farbverlaufsstopp des Farbverlaufs mit der in der Zelle **Zelle FillForegnd** angegebenen Farbe erstellt wird. 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Gibt eine Schattierung oder einen Farbton rot zurück, indem der zweite Farbverlaufsstopp auf eine rote Basisfarbe angewendet wird.
  

