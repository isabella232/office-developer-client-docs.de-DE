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
description: Gibt das Dezimaltrennzeichen für das Gebietsschema des aktuellen Benutzers zurück.
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796819"
---
# <a name="decimalsep-function"></a>DECIMALSEP-Funktion

Gibt das Dezimaltrennzeichen für das Gebietsschema des aktuellen Benutzers zurück.
  
## <a name="syntax"></a>Syntax

DECIMALSEP( )
  
## <a name="example"></a>Beispiel

SETF(GETREF(User.Size), Benutzer.wholepart &amp; DECIMALSEP() &amp; Benutzer.fracpart) 
  

