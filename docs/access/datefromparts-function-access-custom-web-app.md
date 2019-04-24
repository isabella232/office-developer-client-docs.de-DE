---
title: DateFromParts-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282122"
---
# <a name="datefromparts-function-access-custom-web-app"></a>DateFromParts-Funktion (Access Custom Web App)

Gibt einen Datumswert für das angegebene Jahr, den Monat und den Tag zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateFromParts** (*Jahr*, *Monat*, *Tag*) 
  
Die **DateFromParts** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Jahr*  <br/> |Integer-Ausdruck, der ein Jahr angibt.  <br/> |
| *Month*  <br/> |Integer-Ausdruck, der einen Monat zwischen 1 und 12 angibt.  <br/> |
| *Day*  <br/> |Integer-Ausdruck, der einen Tag angibt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

**DateFromParts** gibt einen Date-Wert zurück, wobei der Datumsteil auf das angegebene Jahr, den Monat und den angegebenen Tag sowie auf den standardmäßigen Zeitabschnitt festgelegt ist. Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst. Wenn die erforderlichen Argumente NULL sind, wird NULL zurückgegeben. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck verwendet die **DateFromParts** -Funktion, um den ersten Tag des aktuellen Monats zu berechnen. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



