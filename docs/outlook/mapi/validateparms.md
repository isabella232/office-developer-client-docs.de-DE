---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329575"
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
  
> in Gibt die zu überprüfende Methode an. 
    
 _First_
  
> in Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Alle Parameter sind gültig. 
    
MAPI_E_CALL_FAILED 
  
> Mindestens einer der Parameter ist ungültig.
    
## <a name="remarks"></a>Bemerkungen

Parameter, die zwischen MAPI-und Dienstanbietern übergeben werden, werden als richtig angenommen und werden nur mit dem [CheckParms](checkparms.md) -Makro überprüft. Anbieter sollten alle Parameter überprüfen, die von Clientanwendungen übergeben wurden, aber Clients sollten davon ausgehen, dass MAPI-und Anbieter Parameter korrekt sind. Verwenden Sie das **HR_FAILED** -Makro, um Rückgabewerte zu testen. 
  
 **ValidateParms** wird unterschiedlich aufgerufen, je nachdem, ob der Aufrufcode C oder C++ ist. C++ übergibt einen impliziten Parameter, der als _this_ bezeichnet wird, an jeden Methodenaufruf, der in C explizit wird und die Adresse des Objekts ist. Der erste Parameter, _eMethod_, ist ein Enumerator aus der Schnittstelle und der Methode, die validiert wird, und gibt an, welche Parameter im Stapel zu finden sind. Der zweite Parameter ist für C und C++ unterschiedlich. In C++ wird es _zuerst_aufgerufen und ist der erste Parameter für die validierte Methode. Der zweite Parameter für die Sprache C, _ppThis_, ist die Adresse des ersten Parameters der Methode, bei der es sich immer um einen Objektzeiger handelt. In beiden Fällen gibt der zweite Parameter die Adresse des Beginns der Parameterliste der Methode an und basiert auf _eMethod_, verschiebt den Stapel nach unten und überprüft die Parameter. 
  
Anbieter, die gängige Schnittstellen wie **IMAPITable** und **IMAPIProp** implementieren, sollten Parameter mithilfe der **ValidateParms** -Funktion immer überprüfen, um die Konsistenz aller Anbieter sicherzustellen. Es wurden zusätzliche Parameter Validierungsfunktionen für einige komplexe Parametertypen definiert, die stattdessen entsprechend verwendet werden. In den Referenzthemen finden Sie die folgenden Funktionen: 
  
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
    
Geerbte Methoden verwenden die gleiche Parametervalidierung wie die Schnittstelle, von der Sie erben. Beispielsweise sollte die Parameterüberprüfung für **IMessage** und **IMAPIProp** identisch sein. 
  
## <a name="see-also"></a>Siehe auch



[UlValidateParms](ulvalidateparms.md)

