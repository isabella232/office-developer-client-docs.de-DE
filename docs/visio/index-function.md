---
title: INDEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Gibt die Teilzeichenfolge am Index nullbasierte Position in der durch Trennzeichen getrennten Liste zurück. Oder, wenn der Index außerhalb des gültigen Bereichs, gibt eine leere Zeichenfolge oder das optionale als Argument für Errorvalue bereitgestellt.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797198"
---
# <a name="index-function"></a>INDEX-Funktion

Gibt die Teilzeichenfolge am Speicherort der nullbasierte _Index_ in der durch _Trennzeichen_getrennten _Liste_ zurück. Oder, wenn der Index außerhalb des gültigen Bereichs, gibt eine leere Zeichenfolge oder das optionale als Argument für *Errorvalue* bereitgestellt. 
  
## <a name="syntax"></a>Syntax

INDEX (** *Index* **, "** *Liste* **" [, [** *Trennzeichen* **] [, [** *Errorvalue* **]]]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Position, die gefunden werden soll.  <br/> |
| _list_ <br/> |Erforderlich  <br/> |**String** <br/> |Die Liste, in der gesucht werden soll.  <br/> |
| _delimiter_ <br/> |Optional  <br/> |**String** <br/> | Die Zeichenfolge an, in der _Liste_als Trennzeichen verwendet. Zeichenfolge für ein _Trennzeichen_ kann mehrere Zeichen lang sein und multibyte-Zeichen enthalten. Der Standardwert ist eine durch Semikolons.  <br/> |
| _Fehlerwert_ <br/> |Optional  <br/> |**Nummer** <br/> | Ein benutzerdefinierter Wert, der zurückgegeben wird, wenn sich der Index außerhalb des gültigen Bereichs befindet. Der Standardwert ist eine leere Zeichenfolge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge. 
  
Wenn der Index außerhalb des gültigen Bereichs befindet, gibt Visio eine leere Zeichenfolge oder das optionale als Argument für *Errorvalue* bereitgestellt. 
  
## <a name="example-1"></a>Beispiel 1

INDEX(3,"Katze;Ratte;;Ziege")
  
Gibt "Ziege" zurück.
  
## <a name="example-2"></a>Beispiel 2

INDEX(54,";1;2;3;",,"FEHLER")
  
Gibt "Fehler".
  

