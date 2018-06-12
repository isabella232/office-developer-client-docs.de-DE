---
title: Concat-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790171"
---
# <a name="concat-function-access-custom-web-app"></a>Concat-Funktion (Access benutzerdefinierte Web app)

Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
  
> [!IMPORTANT]
> [!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Concat** (*Wert1*, *Wert2*... [*ValueN*]) 
  
Die Funktion **Verketten** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
|Wert  <br/> |Ein Zeichenfolgenwert, der mit den anderen Werten verkettet werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

**Verketten** verwendet eine unterschiedliche Anzahl von Zeichenfolgenargumenten und verkettet diese zu einer einzigen Zeichenfolge. Mindestens zwei Zeichenfolgenargumente sind erforderlich. Andernfalls wird ein Fehler ausgelöst. 
  
Alle Argumente werden implizit in Zeichenfolgen-Datentypen konvertiert und dann verkettet.
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das Feld MiddleInitial leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen angezeigt.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


