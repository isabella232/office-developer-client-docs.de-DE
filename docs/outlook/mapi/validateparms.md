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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579718"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft eine interne Funktion, um zu überprüfen, dass die Parameter-Clientanwendungen Dienstanbietern vergangen sind. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapival.h  <br/> |
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
  
> [in] Gibt den-Enumeration zurück, die-Methode, um zu überprüfen. 
    
 _Erster_
  
> [in] Zeiger auf das erste Argument im Stapel.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Alle Parameter sind ungültig. 
    
MAPI_E_CALL_FAILED 
  
> Eine oder mehrere der Parameter sind ungültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Übergeben Sie Parameter zwischen MAPI- und Service Provider wird angenommen, dass korrekt und unterzogen werden nur Debug Validierung mit dem Makro [CheckParms](checkparms.md) . Anbieter sollten alle von Clientanwendungen übergebenen Parameter überprüfen, aber Clients sollten davon ausgehen, dass MAPI und Anbieter Parameter richtig sind. Verwenden Sie das Makro **HR_FAILED** , um Rückgabewerte testen. 
  
 **ValidateParms** ist anders aufgerufen, je nachdem, ob der aufrufende Code C oder C++ ist. C++ übergibt einen impliziten Parameter zu jedem Methodenaufruf, die wird explizite in C# und ist die Adresse des Objekts als _diese_ bezeichnet. Der erste Parameter, _eMethod_, ist ein Enumerator, die aus der Benutzeroberfläche und den validierten-Methode und teilt welche Parameter Sie erwarten, auf dem Stapel zu erhalten. Der zweite Parameter ist für C und C++ unterschiedlich. In C++ ist es _ersten_aufgerufen, und es ist der erste Parameter der Methode überprüft wird. Der zweite Parameter für die Sprache C, _PpThis_, ist die Adresse des ersten Parameters an die-Methode, die immer ein Objektzeiger ist. In beiden Fällen der zweite Parameter gibt die Adresse des Anfang der Parameterliste der Methode, und basierend auf _eMethod_, wird der Stapel nach unten verschoben und überprüft die Parameter. 
  
Anbieter für gemeinsame Schnittstellen wie **IMAPITable** und **IMAPIProp** implementieren sollten immer Parameter mithilfe der **ValidateParms** -Funktion, um Stellen Sie sicher, dass Konsistenz für alle Anbieter überprüfen. Zusätzliche Parameter Validierungsfunktionen wurden für einige komplexen Parametertypen entsprechend verwendet werden muss definiert. Finden Sie in den Referenzthemen für die folgenden Funktionen: 
  
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
    
Geerbte Methoden verwenden die gleichen Parameter Überprüfung als Schnittstelle von der sie erben. Beispielsweise sollte der Überprüfung der **IMessage** und **IMAPIProp** Parameter identisch sein. 
  
## <a name="see-also"></a>Siehe auch



[UlValidateParms](ulvalidateparms.md)

