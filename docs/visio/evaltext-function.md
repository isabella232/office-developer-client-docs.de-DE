---
title: EVALTEXT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
ms.localizationpriority: medium
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Wertet den Text in Formname so aus, als wäre er eine Formel und gibt das Ergebnis zurück.
ms.openlocfilehash: 2ba21cc55ea24144396fe4ef029b9a3e1014484a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574300"
---
# <a name="evaltext-function"></a>EVALTEXT Function

Wertet den Text in  _Formname_ so aus, als wäre er eine Formel und gibt das Ergebnis zurück. 
  
## <a name="syntax"></a>Syntax

EVALTEXT(** *shapename!theText* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Zelle, die bei Änderungen an der Textgestaltung des zugeordneten Shapes ausgelöst wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>HinwBemerkungeneise

 Mit _shapename_ kann auf den Text eines anderen Shapes (statt auf den Text des aktuellen Shapes) verwiesen werden. 
  
Wenn kein Text vorhanden ist, ist das Ergebnis 0. Wenn der Text nicht ausgewertet werden kann, gibt die Funktion einen Fehler zurück.
  
## <a name="example"></a>Beispiel

EVALTEXT(Line.2!theText) 
  
Wertet den Text des Shapes Line.2 aus. Wenn Line.2 beispielsweise den Text "4 ft + 0,5 ft" enthält, wird der Wert 4,5 ft zurückgegeben. 
  

