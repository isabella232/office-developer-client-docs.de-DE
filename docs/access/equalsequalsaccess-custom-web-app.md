---
title: Ist gleich (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Vergleicht die Gleichheit zweier Ausdrücke.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790216"
---
# <a name="equals-access-custom-web-app"></a>Ist gleich (Access benutzerdefinierte Web app)

Vergleicht die Gleichheit zweier Ausdrücke.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

`= (Equals)`

*Ausdruck*  =  *Ausdruck* 
  
*Ausdruck*  Ist ein beliebiger gültiger Ausdruck. Wenn die Ausdrücke nicht den gleichen Datentyp aufweisen, muss der Datentyp für einen Ausdruck implizit in den Datentyp des anderen. Die Konvertierung, abhängig von den Regeln der Rangfolge der Datentypen. 
  
## <a name="return-type"></a>Rückgabetyp

**Boolean**
  
## <a name="remarks"></a>Hinweise

Beim Vergleichen von zwei NULL-Ausdrücken ist das Ergebnis TRUE.
  
FALSE führt NULL immer mit einem NULL Wert zu vergleichen.
  

