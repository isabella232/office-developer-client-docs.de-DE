---
title: THEMECBV Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Gibt einen RGB-Wert oder eine ganze Zahl, die einen Index in der Farbpalette des Dokuments darstellt, in dem die Farbe (Anzahl) als Argument übergeben wurde durch den angegebenen Farbton oder eine Schattierung Wert in den Farbverlauf Einstellungen des aktiven Designs gespeichert geändert wurden.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798272"
---
# <a name="themecbv-function"></a>THEMECBV Function

Gibt einen RGB-Wert oder eine ganze Zahl, die einen Index in der Farbpalette des Dokuments darstellt, in dem die Farbe (Anzahl) als Argument übergeben wurde durch den angegebenen Farbton oder eine Schattierung Wert in den Farbverlauf Einstellungen des aktiven Designs gespeichert geändert wurden. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2013 
  
## <a name="syntax"></a>Syntax

 **THEMECBV** ( _Farbe_, _Gradient_stop_number_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Farbe_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Eine Zahl, die einen Index in der Farbpalette des Dokuments darstellt.  <br/> |
| _gradient_stop_number_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Farbverlaufstopp (Farbton oder eine Schattierung) in den Farbverlauf Einstellungen des aktiven Designs auf die Farbe anwenden gespeichert.  <br/> |
   
## <a name="return-value"></a>R�ckgabewert

 **Nummer**
  
## <a name="remarks"></a>Hinweise

> [!NOTE]
> Die THEMECBV-Funktion hat keine Auswirkung auf die Farbe als Argument übergeben wird, wenn die QuickStyle, die mit dem Shape zugewiesen ist keinen Farbverlauf verfügt. 
  
Die Farbverlauf Einstellungen in einem Design sind eine Reihe von nummerierten Farbverlaufstopps, die ein "Aufhellen" (Farbton) oder "Abdunkeln" (Schatten) entsprechen. Diese Graustufen und Farbtöne gelten für eine Basis Farbe, um einen Farbverlauf Effekt zu erstellen.
  
Die **THEMECBV** -Funktion übernimmt eine Farbe Eingabe und gibt die Farbe aus, nachdem es durch den Farbton oder die Schattierung des angegebenen Farbverlaufstopps geändert wurde. Die Farbtöne und Schattierungen stammen das Design-Definition, wenn die aktuelle Schnellformatvorlage für eine graduelle Füllung enthält. Wenn die aktive Schnellformatvorlage keine angegeben wird, dass eine graduelle Füllung oder auf das Shape kein Design festgelegt ist, gibt diese Formel einfach die Farbe, die für das erste Argument übergeben wurde. 
  
## <a name="example"></a>Beispiel

 `THEMECBV(FillForegnd, 5)`
  
Gibt die Farbe erstellt wird, den Farbton oder die Schattierung in der fünften Farbverlaufstopp des Farbverlaufs auf die in die Zelle **FillForegnd** angegebene Farbe angewendet. 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
Gibt eine Schattierung oder einen Farbton durch Anwenden des zweiten Unterbrechungspunkts auf einen Basiskalender Farbe Rot erstellten Rot fest.
  

