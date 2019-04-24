---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316611"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Eigenschaftswert einer oder mehrerer Eigenschaften eines Objekts ab.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Parameter

 _lpPropTagArray_
  
> in Ein Zeiger auf ein Array von Property-Tags, die die Eigenschaften identifizieren, deren Werte abgerufen werden sollen. Der _lpPropTagArray_ -Parameter muss entweder NULL sein, wodurch angegeben wird, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden sollen, oder auf eine [SPropTagArray](sproptagarray.md) -Struktur verweisen, die mindestens ein Property-Tag enthält. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die das Format für Eigenschaften mit dem Typ PT_UNSPECIFIED angibt. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenwerte für diese Eigenschaften sollten im Unicode-Format zurückgegeben werden. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sollten die Zeichenfolgenwerte im ANSI-Format zurückgegeben werden.
    
 _lpcValues_
  
> Out Ein Zeiger auf die Anzahl von Eigenschaftswerten, auf die durch den _lppPropArray_ -Parameter verwiesen wird. Wenn _lppPropArray_ ist, ist der Inhalt des _lpcValues_ -Parameters 0 (null). 
    
 _lppPropArray_
  
> Out Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaftswerte wurden erfolgreich abgerufen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden. Der **aulPropTag** -Member des Eigenschaftswerts für jede nicht verfügbare Eigenschaft hat den Eigenschaftentyp PT_ERROR und den Bezeichner 0 (null). Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> 0 (null) wurde im **cValues** -Element der **SPropTagArray** -Struktur übergeben, auf die durch _lpPropTagArray_verwiesen wurde.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp::** GetProps-Methode ruft die Eigenschaftswerte einer oder mehrerer Eigenschaften eines Objekts ab. 
  
Die Eigenschaftswerte werden in der Reihenfolge zurückgegeben, in der Sie angefordert wurden (die Reihenfolge der Eigenschaften im Eigenschaftentag-Array, auf die durch _lpPropTagArray_ verwiesen wird, entspricht der Reihenfolge im Array von Eigenschaftswert Strukturen, auf die durch _lppPropArray _). 
  
Die in den **aulPropTag** -Elementen des Property-Tag-Arrays angegebenen Eigenschaftentypen geben den Typ des Werts an, der im **value** -Element jeder Eigenschaftswert Struktur zurückgegeben werden soll. Wenn der Aufrufer den Typ einer Eigenschaft jedoch nicht kennt, kann der Typ im **aulPropTag** -Element stattdessen auf PT_UNSPECIFIED festgelegt werden. Beim Abrufen des Werts legt getProps den richtigen Typ im **aulPropTag** -Element der Eigenschaftswert Struktur für die Eigenschaft fest. **** 
  
Wenn Eigenschaftstypen in der **SPropTagArray** in _lpPropTagArray_angegeben werden, haben die Eigenschaftswerte in der **SPropValue** , die in _lppPropArray_ zurückgegeben werden, Typen, die genau mit den angeforderten Typen übereinstimmen, es sei denn, ein Fehlerwert wird zurückgegeben statt. 
  
Zeichenfolgeneigenschaften können einen von zwei Eigenschaftentypen aufweisen: PT_UNICODE zur Darstellung des Unicode-Formats und PT_STRING8 zur Darstellung des ANSI-Formats. Wenn das MAPI_UNICODE-Flag im _ulFlags_ -Parameter festgelegt ist, wird der Wert im Unicode-Format zurückgegeben, wenn GetProps das entsprechende Format für eine String-Eigenschaft nicht ermitteln kann. **** **** GetProps kann in den folgenden Situationen keinen genauen String-Eigenschaftentyp bestimmen: 
  
- Der Parameter _lpPropTagArray_ wird auf NULL festgelegt, um alle Eigenschaften anzufordern. 
    
- Das **aulPropTag** -Element enthält den Wert PT_UNSPECIFIED als Eigenschafts im Property-Tag-Array. 
    
Wenn der Parameter _lpPropTagArray_ auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen, und keine Eigenschaften vorhanden sind, führt GetProps folgende Aktionen aus: **** 
  
- Gibt S_OK zurück.
    
- Legt den count-Wert im **cValues** -Element der Eigenschaftswert Struktur auf 0 fest. 
    
- Legt den Inhalt von _lpcValues_ auf 0 fest. 
    
- Legt _lppPropArray_ auf NULL fest. 
    
 **** GetProps darf keine Eigenschaften mit mehreren Werten zurückgeben, wenn **cValues** auf 0 festgelegt ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion auf, um zunächst Speicher für die [SPropValue](spropvalue.md) -Struktur zu reservieren, auf die von _lpPropTagArray_verwiesen wird; Rufen Sie [MAPIAllocateMore](mapiallocatemore.md) auf, um zusätzlichen Arbeitsspeicher für die Mitglieder der Struktur zu reservieren. 
  
Geben Sie MAPI_W_ERRORS_RETURNED zurück, wenn der Wert für eine oder mehrere der angeforderten Eigenschaften nicht abgerufen werden kann. Legen Sie in der Eigenschaftswert Struktur den Typ im **aulPropTag** -Element auf PT_ERROR und den **Wert** Member auf einen Statuscode fest, der den Fehler beschreibt. Wenn Sie beispielsweise eine Zeichenfolge in Unicode konvertieren und Unicode nicht unterstützen, legen Sie den **Wert** Mitglied auf MAPI_E_BAD_CHARWIDTH. Wenn die Eigenschaft zu hoch ist, legen Sie Sie auf MAPI_E_NOT_ENOUGH_MEMORY. Wenn das Objekt die Eigenschaft nicht unterstützt, legen Sie es auf MAPI_E_NOT_FOUND. 
  
Die Implementierung der getProps-Methode **** eines Remote Transportanbieters muss die Eigenschaftswerte des Ordners für vom Aufrufer angeforderte Eigenschaften zurückgeben. Die Implementierung muss folgende Schritte ausführen: 
  
- Weisen Sie ein Eigenschaftswert Array zu, um zum Aufrufer zurückzukehren, und speichern Sie dessen Adresse im für diesen Zweck übergebenen Parameter value Pointer.
    
- Kopieren Sie die Eigenschaftstags aus den Eigenschaften des Ordners in die Eigenschaftstags im Eigenschafts Wertarray entsprechend dem Array von Property- **** Tags, die an GetProps übergeben werden.
    
- Stellen Sie sicher, dass der Eigenschaftentyp für alle an getProps übergebenen Eigenschaftstags festgelegt ist. **** Der Aufrufer kann einen Eigenschaftentyp von PT_UNSPECIFIED übergeben, in dem Fall, **** dass GetProps den richtigen Eigenschaftentyp für das Eigenschaftentag festlegen muss. 
    
- Legen Sie den Wert jeder Eigenschaft im Eigenschaftswert Array entsprechend dem-Tag fest. Wenn beispielsweise das vom Aufrufer angeforderte Property-Tag **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md)) ist, kann **** GetProps den Wert auf MAPI_FOLDER festlegen. 
    
- Wenn der Aufrufer alle Eigenschaftentags übergibt, die von der Implementierung nicht behandelt werden, können Sie das Property-Tag für diese Eigenschaften auf PT_ERROR festlegen und den Eigenschaftswert auf MAPI_E_NOT_FOUND festlegen.
    
- Gibt S_OK zurück, wenn keine Fehler aufgetreten sind, oder MAPI_W_ERRORS_RETURNED, wenn Fehler auftraten.
    
Die Implementierung der getProps-Methode **** eines Remote Transportanbieters muss mindestens die folgenden Eigenschaften unterstützen: 
  
- **PR_ACCESS** ([Pidtagaccess (](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([Pidtagaccesslevel (](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([Pidtagassociatedcontentcount (](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([Pidtagfoldertype (](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([Pidtagsubfolders (](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie bei Eigenschaften vom Typ PT_OBJECT die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode anstelle **** von GetProps auf. 
  
Für sichere Eigenschaften erwarten Sie Sie nicht, indem Sie getProps mit dem _lppPropTagArray_ -Parameter aufrufen, der auf NULL festgelegt ist. **** Sie müssen den Bezeichner einer sicheren Eigenschaft im **aulPropTag** -Element des Property-Tag-Arrays explizit festlegen, wenn **** Sie GetProps aufrufen. Wann und wie eine sichere Eigenschaft verfügbar ist, liegt beim Dienstanbieter. 
  
Freigeben der zurückgegebenen **SPropValue** -Struktur durch Aufrufen der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion nur, wenn GetProps S_OK oder MAPI_W_ERRORS_RETURNED zurückgibt. **** 
  
Wenn **** GetProps MAPI_W_ERRORS_RETURNED zurückgibt, da der Zugriff auf eine oder mehrere Eigenschaften nicht möglich ist, überprüfen Sie die Eigenschaftentags der zurückgegebenen Eigenschaften. Für die Eigenschaften des Fehlers werden die folgenden Werte in der Eigenschaftswert Struktur festgelegt: 
  
- Der Eigenschaftentyp im **aulPropTag** -Element, der auf PT_ERROR festgelegt ist. 
    
- Der Eigenschaftswert im **Wert** Element, der auf einen Statuscode für den Fehler festgelegt ist, beispielsweise MAPI_E_NOT_FOUND. 
    
Eigenschaften, die fehlschlagen, da Sie zu umfangreich sind, um in der Eigenschaftswert **** Struktur bequem zurückgegeben werden zu können, sind auf MAPI_E_NOT_ENOUGH_MEMORY festgelegt. Dies geschieht NormalerWeise mit String-oder Binary-Eigenschaften vom Typ PT_STRING8, PT_UNICODE oder PT_BINARY, wenn der Wert der Eigenschaft 4 KB oder größer ist. Rufen Sie **IMAPIProp:: OpenProperty** auf, um umfangreiche Eigenschaften abzurufen. 
  
Nicht alle Implementierungen **** von GetProps unterstützen sowohl die Unicode-als auch die ANSI-Formate für Zeichenfolgen. Wenn eine bestimmte Eigenschaft Zeichenfolgenformat Konvertierung erfordert **** und von GetProps nicht unterstützt werden kann, wird der **Wert** für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH festgelegt. 
  
Um zu überprüfen, ob eine PST-Datei eine SharePoint-PST ist, montieren Sie die PST **** -Datei mithilfe von [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md), und rufen Sie dann GetProps für das Nachrichtenspeicherobjekt auf, das diese Eigenschaft Wenn dies der Fall ist, können Sie davon ausgehen, dass die PST-Datei für SharePoint konfiguriert wurde. Wenn dies nicht der Fall ist, wurde die PST-Datei nicht als SharePoint-PST-Datei konfiguriert. 
  
Weitere Informationen zur Verwendung von getProps für den Zugriff auf Eigenschaften finden Sie unter [Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md). ****
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI verwendet die **IMAPIProp::** GetProps-Methode, um alle Eigenschaften eines Objekts abzurufen, indem entweder NULL oder das von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegebene Array im _lpPropTagArray_ -Parameter übergeben wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

