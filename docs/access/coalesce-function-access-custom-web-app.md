---
title: COALESCE-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Gibt den ersten Ausdruck, der nicht aus einer Liste der Argumente NULL ist.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790201"
---
# <a name="coalesce-function-access-custom-web-app"></a>COALESCE-Funktion (Access benutzerdefinierte Web app)

Gibt den ersten Ausdruck, der nicht aus einer Liste der Argumente NULL ist.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**Koaleszieren (COALESCE)** (*Wert*[*Wert*],..., [*Wert*]) 
  
**Coalesce** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Value*  <br/> |Ein Ausdruck.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn alle Argumente NULL sind, gibt **Coalesce** NULL zurück. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck ist als der Überprüfungsregel für eine Tabelle verwendet. Der Ausdruck wird sichergestellt, dass Einträge in den Feldern Vorname, letzte Name, E-Mail, Mobiltelefon, Arbeit, Home Phone, und Telefongesellschaft vorgenommen werden, bevor ein Datensatz ein Commit ausgeführt wird. Wenn eines der aufgelisteten Felder leer sind, gibt die **Coalesce** -Funktion Null, der die Gültigkeitsregel verletzen. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


