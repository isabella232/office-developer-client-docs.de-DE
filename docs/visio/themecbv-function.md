---
title: THEMECBV Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die als Argument übergebene Farbe (Zahl) durch den angegebenen Farbton- oder Schattierungswert geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist.
ms.openlocfilehash: 1d9a95aedee2f04e72bd4868ddfaec149c872b62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603329"
---
# <a name="themecbv-function"></a>THEMECBV Function

Gibt einen RGB-Wert oder eine ganze Zahl zurück, die einen Index in der Farbpalette des Dokuments darstellt, wobei die als Argument übergebene Farbe (Zahl) durch den angegebenen Farbton- oder Schattierungswert geändert wurde, der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **THEMECBV**( _Color_,  _gradient_stop_number_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Erforderlich  <br/> |**Number** <br/> |Eine Zahl, die einen Index in der Farbpalette des Dokuments darstellt.  <br/> |
| _gradient_stop_number_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Farbverlaufstopp (Farbton oder Schatten), der in den Farbverlaufseinstellungen des aktiven Designs gespeichert ist, um auf die Farbe angewendet zu werden.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

 **Number**
  
## <a name="remarks"></a>HinwBemerkungeneise

> [!NOTE]
> Die THEMECBV-Funktion hat nichts mit der Farbe zu tun, die als Argument übergeben wird, wenn der QuickStyle, der der Form zugewiesen ist, keinen Farbverlauf aufweist. 
  
Die Farbverlaufseinstellungen in einem Design sind eine Reihe von nummerierten Farbverlaufsstopps, die einer "Aufhellung" (Farbton) oder "Abdunkelung" (Schatten) entsprechen. Diese Schattierungen und Farbtöne werden auf eine Basisfarbe angewendet, um einen Farbverlaufseffekt zu erzeugen.
  
Die **THEMECBV-Funktion** verwendet eine Farbeingabe und gibt die Farbe aus, nachdem sie durch den Farbton oder Schatten des angegebenen Farbverlaufsstopps geändert wurde. Die Farbtöne und Schattierungen stammen aus der Definition des Designs, wenn die aktuelle Schnellformatvorlage eine Farbverlaufsfüllung enthält. Wenn die aktive Schnellformatvorlage keine Farbverlaufsfüllung angibt oder die Form auf "Kein Design" festgelegt ist, gibt diese Formel einfach die Farbe zurück, die für das erste Argument übergeben wurde. 
  
## <a name="example"></a>Beispiel

 `THEMECBV(FillForegnd, 5)`
  
Gibt die Farbe zurück, die durch Anwenden des Farbtons oder Schattens im fünften Farbverlaufsstopp des Farbverlaufs auf die in der **Zelle FillForegnd** angegebene Farbe erstellt wurde. 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Gibt einen Schattierungs- oder Farbton von Rot zurück, der durch Anwenden des zweiten Farbverlaufsstopps auf eine Basisfarbe von Rot erstellt wird.
  

