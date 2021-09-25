---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d010d325f0668d2ab638544bc02713817491300
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584444"
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
  
> [in] Die Anzahl der Eigenschaftswerte, auf die durch den  _LpPropArray-Parameter_ verwiesen wird. Der  _cValues-Parameter_ darf nicht 0 sein. 
    
 _lpPropArray_
  
> [in] Ein Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die eigenschaftswerte enthalten, die aktualisiert werden sollen. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was bedeutet, dass keine Fehlerinformationen erforderlich sind. Wenn  _lppProblems_ ein gültiger Zeiger für die Eingabe ist, gibt **SetProps** detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehrerer Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich aktualisiert.
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **SetProps:**
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht aktualisiert werden, da sie schreibgeschützt ist und vom Dienstanbieter berechnet wird, der für das Objekt verantwortlich ist.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftstyp ist ungültig.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zuzugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Die Eigenschaft kann nicht aktualisiert werden, da sie größer als die Rpc-Puffergröße (Remote Procedure Call) ist.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der Typ, der von der aufrufenden Implementierung erwartet wird.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ignorieren Sie das **eigenschaftentag PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) und alle Eigenschaften mit einem Typ von **PT_ERROR**. Nehmen Sie keine Änderungen vor oder melden Sie keine Probleme in der **SPropProblemArray-Struktur.** 
  
Gibt MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Eigenschaftswertarray enthalten ist. Geben Sie diesen Fehler auch zurück, wenn eine Eigenschaft mit mehreren Werten im Array enthalten ist und **deren cValues-Element** auf 0 festgelegt ist. 
  
Wenn der Aufruf insgesamt erfolgreich ist, jedoch Probleme beim Festlegen einiger Eigenschaften auftreten, geben Sie S_OK zurück und fügen Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray-Struktur** ein, auf die der  _lppProblems-Parameter_ zeigt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Je nach Dienstanbieter können Sie möglicherweise auch den Eigenschaftentyp ändern, indem Sie ein Eigenschaftstag übergeben, das einen anderen Typ enthält als zuvor mit einem bestimmten Eigenschaftenbezeichner verwendet wurde.
  
Wenn Sie ein Eigenschaftstag für eine Eigenschaft einschließen, die vom Objekt nicht unterstützt wird und die Implementierung von **SetProps** die Erstellung neuer Eigenschaften ermöglicht, wird die Eigenschaft dem Objekt hinzugefügt. Jeder vorherige Wert, der mit dem Eigenschaftsbezeichner gespeichert wurde, der für die neue Eigenschaft verwendet wurde, wird verworfen. 
  
Beachten Sie, dass der S_OK Rückgabewert nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden. Einige Anbieter speichern **SetProps-Aufrufe** zwischen, bis sie einen Aufruf erhalten, der einen Anbietereingriff erfordert, z. B. [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::GetProps.](imapiprop-getprops.md) Daher ist es möglich, Fehlerwerte zu erhalten, die sich auf den **SetProps-Aufruf** mit den späteren Aufrufen beziehen. 
  
If **SetProps** returns S_OK, check the **SPropProblemArray** structure pointed to by  _lppProblems_ for problems updating individual properties. Wenn **SetProps** einen Fehler zurückgibt, überprüfen Sie nicht das Eigenschaftsproblemarray. Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode](imapiprop-getlasterror.md) des Objekts auf. 
  
Beim Aktualisieren großer Eigenschaften kann **SetProps** fehlschlagen und MAPI_E_NOT_ENOUGH_MEMORY zurückgeben. Es gibt keine maximale Größe für Eigenschaften, und unterschiedliche Objekte können unterschiedliche Grenzwerte haben. Wenn Sie mit potenziell großen Eigenschaften umgehen, sollten Sie darauf vorbereitet sein, die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit IID_IStream als Schnittstellenbezeichner aufzurufen, wenn **SetProps** diesen Fehlerwert zurückgibt. 
  
Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um die **SPropProblemArray-Struktur freizulösen.** 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI verwendet die **IMAPIProp::SetProps-Methode,** um eine Eigenschaft zurück in ein Objekt zu schreiben, nachdem die Eigenschaft bearbeitet wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

