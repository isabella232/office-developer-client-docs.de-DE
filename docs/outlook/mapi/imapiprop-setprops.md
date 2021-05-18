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
  
> [in] Die Anzahl der Eigenschaftswerte, auf die der  _lpPropArray-Parameter_ verweist. Der  _cValues-Parameter_ darf nicht 0 sein. 
    
 _lpPropArray_
  
> [in] Ein Zeiger auf ein Array von [SPropValue-Strukturen,](spropvalue.md) die Eigenschaftswerte enthalten, die aktualisiert werden sollen. 
    
 _lppProblems_
  
> [in, out] Bei der Eingabe ein Zeiger auf einen Zeiger auf eine [SPropProblemArray-Struktur;](spropproblemarray.md) andernfalls NULL, was angibt, dass keine Fehlerinformationen benötigt werden. Wenn  _lppProblems ein_ gültiger Zeiger auf Eingaben ist, gibt **SetProps** detaillierte Informationen zu Fehlern beim Aktualisieren einer oder mehreren Eigenschaften zurück. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaften wurden erfolgreich aktualisiert.
    
Die folgenden Werte können in der **SPropProblemArray-Struktur** zurückgegeben werden, jedoch nicht als Rückgabewerte für **SetProps:**
  
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
MAPI_E_COMPUTED 
  
> Die Eigenschaft kann nicht aktualisiert werden, da sie schreibgeschützt ist und vom Dienstanbieter berechnet wird, der für das Objekt zuständig ist.
    
MAPI_E_INVALID_TYPE 
  
> Der Eigenschaftentyp ist ungültig.
    
MAPI_E_NO_ACCESS 
  
> Es wurde versucht, ein schreibgeschütztes Objekt zu ändern oder auf ein Objekt zu zugreifen, für das der Benutzer nicht über ausreichende Berechtigungen verfügt.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Die Eigenschaft kann nicht aktualisiert werden, da sie größer als die Größe des RPC-Puffers (Remote Procedure Call) ist.
    
MAPI_E_UNEXPECTED_TYPE 
  
> Der Eigenschaftstyp ist nicht der Typ, der von der aufrufenden Implementierung erwartet wird.
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Ignorieren Sie **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md))-Eigenschaftstag und alle Eigenschaften mit dem Typ **PT_ERROR**. Nehmen Sie keine Änderungen vor oder melden Sie keine Probleme in der **SPropProblemArray-Struktur.** 
  
Gibt MAPI_E_INVALID_PARAMETER zurück, wenn eine Eigenschaft vom Typ **PT_OBJECT** im Eigenschaftenwertarray enthalten ist. Geben Sie diesen Fehler auch zurück, wenn eine Eigenschaft mit mehreren Wert im Array enthalten ist und der **cValues-Member** auf 0 festgelegt ist. 
  
Wenn der Aufruf insgesamt erfolgreich ist, es jedoch Probleme beim Festlegen einiger Eigenschaften gibt, geben Sie S_OK zurück, und geben Sie Informationen zu den Problemen in den entsprechenden Eintrag der **SPropProblemArray-Struktur** ein, auf die der  _lppProblems-Parameter_ verweist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Je nach Dienstanbieter können Sie den Eigenschaftentyp auch ändern, indem Sie ein Eigenschaftentag übergeben, das einen anderen Typ enthält als zuvor mit einer bestimmten Eigenschafts-ID verwendet wurde.
  
Wenn Sie ein Eigenschaftstag für eine Eigenschaft hinzufügen, die vom Objekt nicht unterstützt wird und die Implementierung von **SetProps** die Erstellung neuer Eigenschaften ermöglicht, wird die Eigenschaft dem Objekt hinzugefügt. Alle vorherigen Werte, die mit dem Eigenschaftenbezeichner gespeichert wurden, der für die neue Eigenschaft verwendet wurde, werden verworfen. 
  
Beachten Sie, dass S_OK Rückgabewert nicht garantiert, dass alle Eigenschaften erfolgreich aktualisiert wurden. Einige Anbieter **zwischenspeichern SetProps-Anrufe,** bis sie einen Anruf erhalten, für den ein Anbietereingriff erforderlich ist, z. B. [IMAPIProp::SaveChanges](imapiprop-savechanges.md) oder [IMAPIProp::GetProps](imapiprop-getprops.md). Daher können Fehlerwerte empfangen werden, die sich auf den **SetProps-Aufruf** mit den späteren Aufrufen beziehen. 
  
Wenn **SetProps** S_OK, überprüfen Sie die **SPropProblemArray-Struktur,** auf die von  _lppProblems_ verwiesen wird, auf Probleme beim Aktualisieren einzelner Eigenschaften. Wenn **SetProps** einen Fehler zurückgibt, überprüfen Sie das Eigenschaftenproblemarray nicht. Rufen Sie stattdessen die [IMAPIProp::GetLastError-Methode des Objekts](imapiprop-getlasterror.md) auf. 
  
Beim Aktualisieren großer Eigenschaften **kann SetProps** fehler- und MAPI_E_NOT_ENOUGH_MEMORY. Es gibt keine maximale Größe für Eigenschaften, und unterschiedliche Objekte können unterschiedliche Grenzwerte haben. Wenn Sie mit potenziell großen Eigenschaften zu tun haben, können Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit IID_IStream als Schnittstellenbezeichner aufrufen, wenn **SetProps** diesen Fehlerwert zurückgibt. 
  
Rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um die **SPropProblemArray-Struktur frei** zu geben. 
  
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

