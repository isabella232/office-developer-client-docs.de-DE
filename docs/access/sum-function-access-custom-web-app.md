---
title: SUM-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Gibt die Summe aller Werte im Ausdruck zurück.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790373"
---
# <a name="sum-function-access-custom-web-app"></a>SUM-Funktion (Access benutzerdefinierte Web app)

Gibt die Summe aller Werte im Ausdruck zurück.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

 **Summe** (*NumericExpression*) 
  
Die **Sum** -Funktion enthält das folgende Argument. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *NumericExpression*  <br/> |Ein Ausdruck, identifiziert das Feld mit den numerischen Daten, den, die Sie hinzufügen möchten, oder ein Ausdruck, der mithilfe der Daten in diesem Feld eine Berechnung ausgeführt wird. Zu den Operanden von *NumericExpression* zählen der Name des Tabellenfelds, eine Konstante oder eine Funktion (die integrierte oder benutzerdefinierte sein kann jedoch keine der anderen SQL-Aggregatfunktionen).  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **Sum** -Funktion ignoriert Datensätze, die Null-Werte enthalten. 
  
Die **Sum** -Funktion kann nur bei numerischen Spalten verwendet werden. 
  

