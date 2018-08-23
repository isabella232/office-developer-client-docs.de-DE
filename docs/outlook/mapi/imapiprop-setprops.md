---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 93bfcce9c45a4c6fd4d57be8c1222be286e0a945
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592031"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Aktualisiert eine oder mehrere Eigenschaften.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameter

 _cValues_
  
> [in] Die Anzahl der Eigenschaftswerte, die auf den durch den Parameter _LpPropArray_ verwiesen. Der Parameter _cValues_ darf nicht 0 sein. 
    
 _lpPropArray_
  
> [in] Ein Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die enthalten Eigenschaftswerte aktualisiert werden. 
    
 _lppProblems_
  
> [in, out] Bei Eingabe einen Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur. andernfalls NULL zurück, der keine Notwendigkeit zur Fehlerinformationen angibt. Wenn _LppProblems_ einen gültigen Zeiger für die Eingabe ist, gibt **SetProps** detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich aktualisiert.
    
Die folgenden Werte können in der Struktur **SPropProblemArray** , aber nicht als Rückgabewerte für **SetProps**zurückgegeben werden:
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht aktualisiert werden, da es schreibgeschützt ist berechnet, indem der Dienstanbieter, der für das Objekt zuständig ist.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für den der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Die Eigenschaft kann nicht aktualisiert werden, da es größer als die Größe des Puffers Remoteprozeduraufruf Remoteprozeduraufruf (RPC) ist.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht von der aufrufenden Implementierung erwartet.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ignorieren Sie das Eigenschafts-Tag **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) und alle Eigenschaften mit einem **PT_ERROR**. Stellen Sie in der Struktur **SPropProblemArray** nicht geändert oder Probleme melden. 
  
MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Array-Wert Eigenschaft enthalten ist. Auch zurückgeben Sie, dass dieser Fehler, wenn eine mehrwertige Eigenschaft in das Array und seine Member **cValues** einbezogen wird auf 0 gesetzt ist. 
  
Wenn der Aufruf erfolgreich insgesamt ist, aber es Probleme treten mit dem einige der Eigenschaften festlegen, wird zurückgegeben Sie S_OK, und platzieren Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray** -Struktur, der auf der _LppProblems_ -Parameter verweist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Je nach den Dienstanbieter können Sie auch möglicherweise so ändern Sie den Eigenschaftentyp, indem Sie eine Eigenschaftentag, das einen anderen Typ enthält, als vorher mit einem bestimmten Eigenschaftenbezeichner verwendet wurde übergeben.
  
Wenn Sie eine Eigenschaftentag für eine Eigenschaft, die durch das Objekt nicht unterstützt wird und die Implementierung der **SetProps** die Erstellung von neuen Eigenschaften ermöglicht, ist die Eigenschaft auf das Objekt hinzugefügt. Alle vorherigen Werte gespeichert, mit der Bezeichner, der für die neue Eigenschaft verwendet wurde, wird verworfen. 
  
Beachten Sie, dass der Rückgabewert S_OK nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden. Einige Anbieter cache **SetProps** Anrufe, bis sie einen Anruf entgegen, der vom Anbieter Eingriff, beispielsweise [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md)erforderlich sind. Aus diesem Grund ist es möglich, Fehlerwerte erhalten, die für den Aufruf der **SetProps** mit spätere Aufrufe beziehen. 
  
Wenn **SetProps** S_OK zurückgegeben wird, überprüfen Sie die **SPropProblemArray** -Struktur, die auf den _LppProblems_ für Probleme bei der Aktualisierung der einzelner Eigenschaften. Wenn **SetProps** einen Fehler zurückgegeben wird, überprüfen Sie das Problem Array-Eigenschaft nicht. Rufen Sie stattdessen das Objekt [IMAPIProp::GetLastError](imapiprop-getlasterror.md) -Methode. 
  
Beim Aktualisieren großer Eigenschaften können **SetProps** fehl und MAPI_E_NOT_ENOUGH_MEMORY zurückzugeben. Es wurde keine maximale Größe für Eigenschaften, und verschiedene Objekte können unterschiedliche Grenzwerte haben. Wenn Sie mit potenziell großen-Eigenschaften arbeiten, bereiten Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit IID_IStream als Schnittstellenbezeichner aufrufen, **SetProps** dieser Fehlerwert zurück. 
  
Rufen Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um die Struktur **SPropProblemArray** frei. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::SetProps** -Methode zum Zurückschreiben einer Eigenschaft zu einem Objekt nach die Eigenschaft bearbeitet wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

