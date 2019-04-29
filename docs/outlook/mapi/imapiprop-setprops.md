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
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412618"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
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
  
> in Die Anzahl der Eigenschaftswerte, auf die durch den _lpPropArray_ -Parameter verwiesen wird. Der _cValues_ -Parameter darf nicht 0 sein. 
    
 _lpPropArray_
  
> in Ein Zeiger auf ein Array von [SPropValue](spropvalue.md) -Strukturen, die Eigenschaftswerte enthalten, die aktualisiert werden sollen. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray](spropproblemarray.md) -Struktur; andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn _lppProblems_ ein gültiger Zeiger auf der Eingabe ist **** , gibt SetProps detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich aktualisiert.
    
Die folgenden Werte können in der **SPropProblemArray** -Struktur zurückgegeben werden, jedoch nicht als Rückgabewerte für SetProps: ****
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht aktualisiert werden, da sie schreibgeschützt ist und vom Dienstanbieter berechnet wird, der für das Objekt verantwortlich ist.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Die Eigenschaft kann nicht aktualisiert werden, da Sie größer als die RPC-Puffergröße (Remote Procedure Call) ist.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftentyp ist nicht der Typ, der von der aufrufenden Implementierung erwartet wird.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ignorieren Sie das **PR_NULL** ([pidtagnull (](pidtagnull-canonical-property.md))-Eigenschaftentag und alle Eigenschaften mit einem Typ von **PT_ERROR**. Nehmen Sie keine Änderungen vor, oder melden Sie Probleme in der **SPropProblemArray** -Struktur. 
  
Geben Sie MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Eigenschaftswert Array enthalten ist. Geben Sie auch diesen Fehler zurück, wenn eine mehrwertige Eigenschaft im Array enthalten ist und dessen **cValues** -Element auf 0 festgelegt ist. 
  
Wenn der Aufruf insgesamt erfolgreich ist, aber Probleme beim Festlegen einiger Eigenschaften auftreten, geben Sie S_OK zurück, und setzen Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray** -Struktur, auf die der _lppProblems_ -Parameter zeigt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Je nach Dienstanbieter können Sie möglicherweise auch den Eigenschaftentyp ändern, indem Sie ein Property-Tag übergeben, das einen anderen Typ als der zuvor mit einem angegebenen Eigenschaftenbezeichner verwendete ist.
  
Wenn Sie ein Property-Tag für eine Eigenschaft einfügen, die vom Objekt nicht unterstützt wird und die Implementierung **** von SetProps die Erstellung neuer Eigenschaften zulässt, wird die Eigenschaft dem Objekt hinzugefügt. Jeder vorherige Wert, der mit dem Eigenschaftenbezeichner gespeichert wurde, der für die neue Eigenschaft verwendet wurde, wird verworfen. 
  
Beachten Sie, dass der S_OK-Rückgabewert nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden. Einige Anbieter speichern **** SetProps-Aufrufe, bis Sie einen Aufruf erhalten, der eine Anbieter Intervention erfordert, wie [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::](imapiprop-getprops.md)GetProps. Daher ist es möglich, Fehlerwerte zu erhalten, die sich auf **** den SetProps-Aufruf mit den späteren Aufrufen beziehen. 
  
Wenn **** SetProps S_OK zurückgibt, überprüfen Sie die **SPropProblemArray** -Struktur, auf die durch _lppProblems_ für Probleme beim Aktualisieren einzelner Eigenschaften verwiesen wird. Wenn **** SetProps einen Fehler zurückgibt, überprüfen Sie nicht das Problem Array der Eigenschaft. Rufen Sie stattdessen die [IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) -Methode des Objekts auf. 
  
Beim Aktualisieren von umfangreichen **** Eigenschaften können SetProps fehlschlagen und MAPI_E_NOT_ENOUGH_MEMORY zurückgeben. Es gibt keine maximale Größe für Eigenschaften, und verschiedene Objekte können unterschiedliche Begrenzungen aufweisen. Wenn Sie potenziell große Eigenschaften behandeln, müssen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit IID_IStream als Schnittstellenbezeichner aufrufen, wenn SetProps diesen Fehlerwert zurückgibt. **** 
  
Rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um die **SPropProblemArray** -Struktur freizugeben. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Eingeschaften. cpp  <br/> |CPropertyEditor:: WriteSPropValueToObject  <br/> |MFCMAPI verwendet die **IMAPIProp::** SetProps-Methode, um eine Eigenschaft zurück in ein Objekt zu schreiben, nachdem die Eigenschaft bearbeitet wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

