---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d767eae393e31a2c55dbafe0a608bbbc121e60c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623887"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion auf, um die Parameter zu überprüfen, die Clientanwendungen an Dienstanbieter übergeben haben. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapival.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parameter

 _eMethod_
  
> [in] Gibt die zu überprüfende Methode anhand der Aufzählung an. 
    
 _First_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Parameter sind gültig. 
    
MAPI_E_CALL_FAILED 
  
> Mindestens einer der Parameter ist ungültig.
    
## <a name="remarks"></a>Bemerkungen

Parameter, die zwischen MAPI und Dienstanbietern übergeben werden, werden als korrekt angenommen und werden nur mit dem [CheckParms-Makro](checkparms.md) einer Debugüberprüfung unterzogen. Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, clients sollten jedoch davon ausgehen, dass MAPI- und Anbieterparameter korrekt sind. Verwenden Sie das **makro HR_FAILED,** um Rückgabewerte zu testen. 
  
 **ValidateParms** wird unterschiedlich aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist. C++ übergibt einen impliziten Parameter, der als  _dieser_ bezeichnet wird, an jeden Methodenaufruf, der in C explizit wird und die Adresse des Objekts ist. Der erste Parameter,  _eMethod,_ ist ein Enumerator, der aus der Schnittstelle und Methode erstellt wird, die überprüft wird, und gibt an, welche Parameter im Stapel zu finden sind. Der zweite Parameter unterscheidet sich für C und C++. In C++ heißt es  _"First"_ und ist der erste Parameter für die Methode, die überprüft wird. Der zweite Parameter für die Sprache C(  _ppThis_) ist die Adresse des ersten Parameters für die Methode, bei der es sich immer um einen Objektzeiger handelt. In beiden Fällen gibt der zweite Parameter die Adresse des Anfangs der Parameterliste der Methode an. Basierend auf  _eMethod_ wird der Stapel nach unten verschoben und die Parameter überprüft. 
  
Anbieter, die allgemeine Schnittstellen wie **IMAPITable** und **IMAPIProp** implementieren, sollten parameter immer mithilfe der **ValidateParms-Funktion** überprüfen, um die Konsistenz für alle Anbieter sicherzustellen. Für einige komplexe Parametertypen, die stattdessen verwendet werden sollen, wurden zusätzliche Parameterüberprüfungsfunktionen definiert. Die folgenden Funktionen finden Sie in den Referenzthemen: 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
Geerbte Methoden verwenden die gleiche Parameterüberprüfung wie die Schnittstelle, von der sie erben. Beispielsweise sollte die Parameterüberprüfung für **IMessage** und **IMAPIProp** identisch sein. 
  
## <a name="see-also"></a>Siehe auch



[UlValidateParms](ulvalidateparms.md)

