---
title: / (Divide) (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Teilt eine Zahl durch eine andere.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435187"
---
# <a name="-divide-access-custom-web-app"></a>/ (Divide) (Benutzerdefinierte Access-Web-App)

Teilt eine Zahl durch eine andere.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *dividend*   /   *divisor* 
  
 *dividend*  Ist der numerische Ausdruck, der unterteilt werden soll. Kann ein beliebiger gültiger Ausdruck eines beliebigen Datentyps der numerischen Datentypkategorie sein, mit Ausnahme des Datentyps datetime. 
  
 *Divisor*  Ist der numerische Ausdruck, durch den die Dividende dividieren wird. Kann ein beliebiger gültiger Ausdruck eines beliebigen Datentyps der numerischen Datentypkategorie sein, mit Ausnahme des Datentyps datetime. 
  
## <a name="return-type"></a>Rückgabetyp

Gibt den Datentyp des Arguments mit der höheren Rangfolge zurück. 
  
Wenn eine  *ganzzahlige*  Dividende durch einen ganzzahligen  *Divisor*  geteilt wird, ist das Ergebnis eine ganze Zahl, die einen Bruchteil des Ergebnisses abgeschnitten hat. 
  
## <a name="remarks"></a>Hinweise

Der tatsächliche Wert, der vom /-Operator zurückgegeben wird, ist der Quotient des ersten Ausdrucks dividiert durch den zweiten Ausdruck.
  

