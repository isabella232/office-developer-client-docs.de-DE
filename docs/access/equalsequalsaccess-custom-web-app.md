---
title: Equals(Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Vergleicht die Gleichheit zweier Ausdrücke.
ms.openlocfilehash: 7dbca163a1fb9c49b5557e810eeecf978f999c97
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588525"
---
# <a name="equals-access-custom-web-app"></a>Gleich (benutzerdefinierte Access-Web-App)

Vergleicht die Gleichheit zweier Ausdrücke.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

`= (Equals)`

*Ausdruck*   =   *Ausdruck* 
  
*expression*  Ein beliebiger gültiger Ausdruck. Wenn die Ausdrücke nicht denselben Datentyp aufweisen, muss der Datentyp für einen Ausdruck implizit in den Datentyp des anderen datentyps konvertierbar sein. Die Konvertierung ist von den Regeln der Rangfolge der Datentypen abhängig. 
  
## <a name="return-type"></a>Rückgabetyp

**Boolean**
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie zwei NULL-Ausdrücke vergleichen, ist das Ergebnis TRUE.
  
Der Vergleich von NULL mit einem Wert ungleich NULL führt immer zu FALSE.
  

