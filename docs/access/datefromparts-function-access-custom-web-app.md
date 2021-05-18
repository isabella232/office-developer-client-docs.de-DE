---
title: DateFromParts-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423223"
---
# <a name="datefromparts-function-access-custom-web-app"></a>DateFromParts-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateFromParts** (*Year*, *Month*, *Day*) 
  
Die **DateFromParts-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Jahr*  <br/> |Ganzzahliger Ausdruck, der ein Jahr an gibt.  <br/> |
| *Month*  <br/> |Ganzzahliger Ausdruck, der einen Monat von 1 bis 12 an gibt.  <br/> |
| *Day*  <br/> |Ganzzahliger Ausdruck, der einen Tag an gibt.  <br/> |
   
## <a name="remarks"></a>Hinweise

**DateFromParts** gibt einen Datumswert zurück, bei dem der Datumsteil auf das angegebene Jahr, den Monat und den Tag und den Zeitteil auf den Standardwert festgelegt ist. Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst. Wenn erforderliche Argumente null sind, wird NULL zurückgegeben. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck verwendet die **DateFromParts-Funktion,** um den ersten Tag des aktuellen Monats zu berechnen. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



