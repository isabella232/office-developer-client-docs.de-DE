---
title: OR (Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Kombiniert zwei Bedingungen. Gibt TRUE zurück, wenn eine der beiden Bedingungen wahr ist.
ms.openlocfilehash: 18fefc4f5e17f86ac4a307256f8a5b3a6887cdbe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631531"
---
# <a name="or-access-custom-web-app"></a>OR (Benutzerdefinierte Access-Web-App)

Kombiniert zwei Bedingungen. Gibt TRUE zurück, wenn eine der beiden Bedingungen wahr ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *BooleanExpression* **oder** *BooleanExpression* 
  
Der Operator **"Or"** verwendet das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Ein beliebiger gültiger Ausdruck, der TRUE oder FALSE zurückgibt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn in einer Anweisung mehrere logische  Operatoren verwendet werden, werden Or-Operatoren nach **And-Operatoren** ausgewertet. Sie können die Reihenfolge der Auswertung jedoch mithilfe von Klammern ändern. 
  
In der folgenden Tabelle ist das Ergebnis des Operators **"Or"** dargestellt. 
  
||**STIMMT**|**FALSE**|
|:-----|:-----|:-----|
|**STIMMT** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

