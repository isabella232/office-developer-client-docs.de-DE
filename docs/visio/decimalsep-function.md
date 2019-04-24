---
title: DECIMALSEP-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Gibt die Dezimaltrennzeichen-Zeichenfolge für das aktuelle Benutzergebietsschema zurück.
ms.openlocfilehash: 8a59e7331fd51cf5426b5e2cdd64e3c5a22334b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360305"
---
# <a name="decimalsep-function"></a>DECIMALSEP-Funktion

Gibt die Dezimaltrennzeichen-Zeichenfolge für das aktuelle Benutzergebietsschema zurück.
  
## <a name="syntax"></a>Syntax

DECIMALSEP( )
  
## <a name="example"></a>Beispiel

SETF (GETREF (User. Size), User. wholePart &amp; DECIMALSEP () &amp; User. fracPart) 
  

