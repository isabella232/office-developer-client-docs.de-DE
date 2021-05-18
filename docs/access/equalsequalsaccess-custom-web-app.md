---
title: Equals(Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Vergleicht die Gleichheit von zwei Ausdrücken.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408929"
---
# <a name="equals-access-custom-web-app"></a>Gleich (benutzerdefinierte Access-Web-App)

Vergleicht die Gleichheit von zwei Ausdrücken.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

`= (Equals)`

*Ausdruck*   =   *Ausdruck* 
  
*expression*  Ein beliebiger gültiger Ausdruck. Wenn die Ausdrücke nicht denselben Datentyp haben, muss der Datentyp für einen Ausdruck implizit in den Datentyp des anderen konvertiert werden. Die Konvertierung ist von den Regeln der Rangfolge der Datentypen abhängig. 
  
## <a name="return-type"></a>Rückgabetyp

**Boolean**
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie zwei NULL-Ausdrücke vergleichen, ist das Ergebnis TRUE.
  
Der Vergleich von NULL mit einem Nicht-NULL-Wert führt immer zu FALSE.
  

