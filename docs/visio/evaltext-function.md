---
title: EVALTEXT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Wertet den Text in Shapename so aus, als ob er eine Formel wäre, und gibt das Ergebnis zurück.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329050"
---
# <a name="evaltext-function"></a>EVALTEXT Function

Wertet den Text __ in Shapename so aus, als ob er eine Formel wäre, und gibt das Ergebnis zurück. 
  
## <a name="syntax"></a>Syntax

EVALTEXT (* * *Shapename! DerText* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Shapename! DerText_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Zelle, die bei Änderungen an der Textgestaltung des zugeordneten Shapes ausgelöst wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

 Mit _shapename_ kann auf den Text eines anderen Shapes (statt auf den Text des aktuellen Shapes) verwiesen werden. 
  
Wenn kein Text vorhanden ist, ist das Ergebnis 0. Wenn der Text nicht ausgewertet werden kann, gibt die Funktion einen Fehler zurück.
  
## <a name="example"></a>Beispiel

EVALTEXT (Leitung 2! DerText) 
  
Wertet den Text des Shapes Line.2 aus. Wenn Line.2 beispielsweise den Text "4 ft + 0,5 ft" enthält, wird der Wert 4,5 ft zurückgegeben. 
  

