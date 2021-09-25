---
title: Verkettungsfunktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
ms.openlocfilehash: 76e303659ea72a244ad83e12342f00d12c23bf09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573347"
---
# <a name="concat-function-access-custom-web-app"></a>Verkettungsfunktion (benutzerdefinierte Access-Web-App)

Gibt eine Zeichenfolge zurück, die das Ergebnis der Kombination von zwei oder mehr Zeichenfolgenwerte ist.
  
> [!IMPORTANT]
> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen. 
  
## <a name="syntax"></a>Syntax

**Verketten** (*Wert1*, *Wert2*, ... [*ValueN*]) 
  
Die Funktion **Verketten** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
|Wert  <br/> |Ein Zeichenfolgenwert, der mit den anderen Werten verkettet werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

**Verketten** verwendet eine unterschiedliche Anzahl von Zeichenfolgenargumenten und verkettet diese zu einer einzigen Zeichenfolge. Mindestens zwei Zeichenfolgenargumente sind erforderlich. Andernfalls wird ein Fehler ausgelöst. 
  
Alle Argumente werden implizit in Zeichenfolgen-Datentypen konvertiert und dann verkettet.
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck kann verwendet werden, um den vollständigen Namen einer Person anzuzeigen, für welche die Tabelle die Felder "LastName", "FirstName" und "MiddleInitial" enthält. Wenn das MiddleInitial-Feld leer ist, werden nur die Felder FirstName und LastName kombiniert, um den vollständigen Namen anzuzeigen.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


