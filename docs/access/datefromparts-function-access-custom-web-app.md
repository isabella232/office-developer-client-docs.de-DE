---
title: DateFromParts-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Gibt einen Date-Wert für das angegebene Jahr, Monat und Tag zurück.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790163"
---
# <a name="datefromparts-function-access-custom-web-app"></a>DateFromParts-Funktion (Access benutzerdefinierte Web app)

Gibt einen Date-Wert für das angegebene Jahr, Monat und Tag zurück.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateFromParts** (*Jahr*, *Monat*, *Tag*) 
  
Die **DateFromParts** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Jahr*  <br/> |Ein Ausdruck, der ganze Zahl, die einem Jahr angibt.  <br/> |
| *Month*  <br/> |Ein Ausdruck, der ganze Zahl, die einen Monat, von 1 bis 12 angibt.  <br/> |
| *Tag*  <br/> |Ein Ausdruck, der ganze Zahl, die einen Tag angibt.  <br/> |
   
## <a name="remarks"></a>Hinweise

**DateFromParts** gibt einen Date-Wert zurück, mit der Datumsteil auf das angegebene Jahr, Monat und Tag und auf den Standardwert den Zeitbereich festgelegt. Wenn die Argumente nicht gültig sind, wird ein Fehler ausgelöst. Falls erforderlich, dass Argumente null sind, wird NULL zurückgegeben. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck wird die **DateFromParts** -Funktion verwendet, um den ersten Tag des aktuellen Monats zu berechnen. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



