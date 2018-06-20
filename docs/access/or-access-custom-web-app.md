---
title: ODER (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Kombiniert zwei mögliche Ursachen. Gibt TRUE zurück, wenn eine der beiden folgenden Bedingungen zutrifft.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790330"
---
# <a name="or-access-custom-web-app"></a>ODER (Access benutzerdefinierte Web app)

Kombiniert zwei mögliche Ursachen. Gibt TRUE zurück, wenn eine der beiden folgenden Bedingungen zutrifft.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 *Boolescher Ausdruck* **Oder** *Boolescher Ausdruck* 
  
Der **oder** -Operator verwendet das folgende Argument. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Boolescher Ausdruck*  <br/> |Ein beliebiger gültiger Ausdruck, der TRUE oder FALSE zurückgibt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn mehr als ein logischer Operator in einer Anweisung verwendet wird, werden nach **und** Operatoren **oder** Operatoren ausgewertet. Jedoch können Sie die Reihenfolge der Auswertung ändern, indem Sie Klammern verwenden. 
  
Die folgende Tabelle zeigt das Ergebnis des Operators **oder** . 
  
||**"TRUE"**|**"FALSE"**|
|:-----|:-----|:-----|
|**"TRUE"** <br/> |TRUE  <br/> |TRUE  <br/> |
|**"FALSE"** <br/> |TRUE  <br/> |FALSE  <br/> |
   

