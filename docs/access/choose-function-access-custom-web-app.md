---
title: Choose-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
ms.openlocfilehash: 3b2ce27b0bd43c2db1d28f90a0ffbd5c2c206496
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573334"
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
| *IndexNumber*  <br/> |Ein ganzzahliger Ausdruck, der einen 1-basierten Index in der Liste der darauf folgenden Elemente darstellt.  <br/> |
| *Wert*  <br/> |Liste der Werte eines beliebigen Datentyps.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn es sich bei der angegebenen  *IndexNumber*  nicht um eine ganze Zahl handelt, wird der Wert implizit in eine ganze Zahl konvertiert. 
  
Wenn der Indexwert die Grenzen des Arrays von Werten überschreitet, **gibt Choose** NULL zurück. 
  

