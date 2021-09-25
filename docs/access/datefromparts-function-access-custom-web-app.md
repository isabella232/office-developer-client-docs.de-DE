---
title: DateFromParts-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Datumswert für das angegebene Jahr, den angegebenen Monat und den angegebenen Tag zurück.
ms.openlocfilehash: 95839aab8bab46d833e46ef4a33b0f8d0b8ae50c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586453"
---
# <a name="datefromparts-function-access-custom-web-app"></a>DateFromParts-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen Datumswert für das angegebene Jahr, den angegebenen Monat und den angegebenen Tag zurück.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateFromParts** (*Year*, *Month*, *Day*) 
  
Die **DateFromParts-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Jahr*  <br/> |Ganzzahliger Ausdruck, der ein Jahr angibt.  <br/> |
| *Month*  <br/> |Ganzzahliger Ausdruck, der einen Monat zwischen 1 und 12 angibt.  <br/> |
| *Day*  <br/> |Ganzzahliger Ausdruck, der einen Tag angibt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

**DateFromParts** gibt einen Datumswert zurück, wobei der Datumsteil auf das angegebene Jahr, den angegebenen Monat und den angegebenen Tag und den auf den Standardwert festgelegten Zeitteil festgelegt ist. Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst. Wenn erforderliche Argumente NULL sind, wird NULL zurückgegeben. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck verwendet die **DateFromParts-Funktion,** um den ersten Tag des aktuellen Monats zu berechnen. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



