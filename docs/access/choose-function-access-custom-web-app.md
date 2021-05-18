---
title: Choose-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414116"
---
# <a name="choose-function-access-custom-web-app"></a>Choose-Funktion (benutzerdefinierte Access-Web-App)

Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Choose** (*IndexNumber*, *Value*, [*Value_n*]) 
  
Die **Choose-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *IndexNumber*  <br/> |Ein ganzzahliger Ausdruck, der einen 1-basierten Index in der Liste der folgenden Elemente darstellt.  <br/> |
| *Wert*  <br/> |Liste der Werte eines beliebigen Datentyps.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die  *bereitgestellte IndexNumber*  keine ganze Zahl ist, wird der Wert implizit in eine ganze Zahl konvertiert. 
  
Wenn der Indexwert die Grenzen des Wertearrays überschreitet, gibt **Choose NULL** zurück. 
  

