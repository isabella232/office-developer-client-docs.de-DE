---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26ab8d67687038118c2dfbbf8d6fc6baddbdcccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625534"
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
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, die die Eigenschaften identifizieren, deren Werte abgerufen werden sollen. Der  _lpPropTagArray-Parameter_ muss entweder NULL sein, der angibt, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden sollen, oder auf eine [SPropTagArray-Struktur](sproptagarray.md) zeigen, die ein oder mehrere Eigenschaftstags enthält. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für Eigenschaften mit dem Typ PT_UNSPECIFIED angibt. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenwerte für diese Eigenschaften sollten im Unicode-Format zurückgegeben werden. Wenn das flag MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgenwerte im ANSI-Format zurückgegeben werden.
    
 _lpcValues_
  
> [out] Ein Zeiger auf eine Anzahl von Eigenschaftswerten, auf die der  _Parameter "lppPropArray"_ verweist. Wenn  _lppPropArray_ NULL ist, ist der Inhalt des  _lpcValues-Parameters_ Null. 
    
 _lppPropArray_
  
> [out] Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaftswerte wurden erfolgreich abgerufen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden. Das **aulPropTag-Element** des Eigenschaftswerts für jede nicht verfügbare Eigenschaft weist einen Eigenschaftstyp PT_ERROR und einen Bezeichner von Null auf. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md)
    
MAPI_E_INVALID_PARAMETER 
  
> Zero wurde im **cValues-Element** der **SPropTagArray-Struktur** übergeben, auf die von  _lpPropTagArray_ verwiesen wird.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp::GetProps-Methode** ruft die Eigenschaftswerte einer oder mehrerer Eigenschaften eines Objekts ab. 
  
Die Eigenschaftswerte werden in derselben Reihenfolge zurückgegeben, in der sie angefordert wurden (das heißt, die Reihenfolge der Eigenschaften im Eigenschaftentagarray, auf die durch  _lpPropTagArray_ verwiesen wird, entspricht der Reihenfolge im Array der Eigenschaftswertstrukturen, auf die durch  _lppPropArray_ verwiesen wird). 
  
Die in den **aulPropTag-Membern** des Eigenschaftstagarrays angegebenen Eigenschaftstypen geben den Typ des Werts an, der im **Value-Element** jeder Eigenschaftswertstruktur zurückgegeben werden soll. Wenn der Aufrufer jedoch den Typ einer Eigenschaft nicht kennt, kann der Typ im **aulPropTag-Element** stattdessen auf PT_UNSPECIFIED festgelegt werden. Beim Abrufen des **Werts legt GetProps** den richtigen Typ im **aulPropTag-Element** der Eigenschaftswertstruktur für die Eigenschaft fest. 
  
Wenn Eigenschaftstypen im **SPropTagArray** in _lpPropTagArray_ angegeben sind, weisen die Eigenschaftswerte in dem in _lppPropArray_ zurückgegebenen **SPropValue** Typen auf, die genau mit den angeforderten Typen übereinstimmen, es sei denn, es wird stattdessen ein Fehlerwert zurückgegeben. 
  
Zeichenfolgeneigenschaften können einen von zwei Eigenschaftstypen aufweisen: PT_UNICODE zum Darstellen des Unicode-Formats und PT_STRING8 zum Darstellen des ANSI-Formats. Wenn das flag MAPI_UNICODE im  _ulFlags-Parameter_ festgelegt ist, gibt GetProps immer dann seinen Wert im Unicode-Format zurück, wenn **GetProps** das geeignete Format für eine Zeichenfolgeneigenschaft nicht ermitteln kann. **GetProps** kann in den folgenden Situationen keinen genauen Zeichenfolgeneigenschaftstyp ermitteln: 
  
- Der  _Parameter lpPropTagArray_ wird auf NULL festgelegt, um alle Eigenschaften anzufordern. 
    
- Der **aulPropTag-Member** enthält den Wert PT_UNSPECIFIED als Eigenschaftstyp im Eigenschaftentagarray. 
    
Wenn der  _Parameter lpPropTagArray_ auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen und keine Eigenschaften vorhanden sind, führt **GetProps** folgende Aktionen aus: 
  
- Gibt S_OK zurück.
    
- Legt den Wert für die Anzahl im **cValues-Element** der Eigenschaftswertstruktur auf 0 fest. 
    
- Legt den Inhalt von  _lpcValues_ auf 0 fest. 
    
- Legt  _lppPropArray_ auf NULL fest. 
    
 **GetProps** darf keine Mehrfachwerteigenschaften zurückgeben, wobei **cValues** auf 0 festgelegt ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) auf, um zunächst Speicher für die [SPropValue-Struktur zuzuweisen,](spropvalue.md) auf die von  _lpPropTagArray_ verwiesen wird; rufen [Sie MAPIAllocateMore](mapiallocatemore.md) auf, um zusätzlichen Speicher zuzuweisen, der für die Elemente der Struktur benötigt wird. 
  
Geben Sie MAPI_W_ERRORS_RETURNED zurück, wenn Sie den Wert für eine oder mehrere der angeforderten Eigenschaften nicht abrufen können. Legen Sie in der Eigenschaftswertstruktur den Typ im **aulPropTag-Element** auf PT_ERROR und das **Value-Element** auf einen Statuscode fest, der den Fehler beschreibt. Wenn Sie beispielsweise eine Zeichenfolge in Unicode konvertieren müssen und Unicode nicht unterstützen, legen Sie das **Value-Element** auf MAPI_E_BAD_CHARWIDTH fest. Wenn die Eigenschaft zu groß ist, legen Sie sie auf MAPI_E_NOT_ENOUGH_MEMORY fest. Wenn das Objekt die Eigenschaft nicht unterstützt, legen Sie sie auf MAPI_E_NOT_FOUND fest. 
  
Die Implementierung der **GetProps-Methode** durch einen Remotetransportanbieter muss die Eigenschaftswerte des Ordners für eigenschaften zurückgeben, die vom Aufrufer angefordert werden. Die Implementierung muss folgendermaßen vorgehen: 
  
- Weisen Sie dem Aufrufer ein Eigenschaftswertarray zu, und speichern Sie dessen Adresse im Eigenschaftenwertzeigerparameter, der zu diesem Zweck übergeben wurde.
    
- Kopieren Sie die Eigenschaftentags aus den Eigenschaften des Ordners in die Eigenschaftentags im Eigenschaftswertarray gemäß dem Array der Eigenschaftstags, die an **GetProps** übergeben werden.
    
- Stellen Sie sicher, dass der Eigenschaftentyp für alle Eigenschaftentags festgelegt ist, die an **GetProps** übergeben werden. Der Aufrufer kann einen Eigenschaftstyp von PT_UNSPECIFIED übergeben. In diesem Fall muss **GetProps** den richtigen Eigenschaftentyp für dieses Eigenschaftstag festlegen. 
    
- Legen Sie den Wert jeder Eigenschaft im Eigenschaftswertarray entsprechend ihrem Tag fest. Wenn beispielsweise das vom Aufrufer angeforderte Eigenschaftstag **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist, kann **GetProps** den Wert auf MAPI_FOLDER festlegen. 
    
- Wenn der Aufrufer Eigenschaftentags übergibt, die von der Implementierung nicht behandelt werden, können Sie das Eigenschaftstag auf PT_ERROR für diese Eigenschaften festlegen und den Eigenschaftswert auf MAPI_E_NOT_FOUND festlegen.
    
- Gibt S_OK zurück, wenn keine Fehler aufgetreten sind, oder MAPI_W_ERRORS_RETURNED, wenn Fehler aufgetreten sind.
    
Die Implementierung der **GetProps-Methode** durch einen Remote-Transportanbieter muss mindestens die folgenden Eigenschaften unterstützen: 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Rufen Sie für Eigenschaften vom Typ PT_OBJECT die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) anstelle von **GetProps auf.** 
  
Für sichere Eigenschaften erwarten Sie nicht, dass sie durch Aufrufen von **GetProps** abgerufen werden, wobei der  _Parameter lppPropTagArray_ auf NULL festgelegt ist. Sie müssen den Bezeichner einer sicheren Eigenschaft explizit im **aulPropTag-Element** des Eigenschaftentagarrays festlegen, wenn Sie **GetProps** aufrufen. Wann und wie eine sichere Eigenschaft verfügbar ist, liegt beim Dienstanbieter. 
  
Geben Sie die **zurückgegebene SPropValue-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) nur aufrufen, wenn **GetProps** S_OK oder MAPI_W_ERRORS_RETURNED zurückgibt. 
  
If **GetProps** returns MAPI_W_ERRORS_RETURNED because it could not access one or more properties, check the property tags of the returned properties. Für die fehlerhaften Eigenschaften werden die folgenden Werte in der Eigenschaftswertstruktur festgelegt: 
  
- Der Eigenschaftstyp im **aulPropTag-Member,** der auf PT_ERROR festgelegt ist. 
    
- Der Eigenschaftswert im **Value-Element,** der auf einen Statuscode für den Fehler festgelegt ist, z. B. MAPI_E_NOT_FOUND. 
    
Eigenschaften, die fehlschlagen, weil sie zu groß sind, um bequem in der Eigenschaftswertstruktur zurückgegeben zu werden, haben ihren **Wertmember** auf MAPI_E_NOT_ENOUGH_MEMORY festgelegt. Dies geschieht in der Regel bei Zeichenfolgen- oder binären Eigenschaften vom Typ PT_STRING8, PT_UNICODE oder PT_BINARY, wenn der Wert der Eigenschaft 4 KB oder größer ist. Rufen Sie **IMAPIProp::OpenProperty** auf, um große Eigenschaften abzurufen. 
  
Nicht alle Implementierungen von **GetProps** unterstützen sowohl das Unicode- als auch das ANSI-Format für Zeichenzeichenfolgen. Wenn eine bestimmte Eigenschaft eine Konvertierung im Zeichenfolgenformat erfordert und **GetProps** sie nicht unterstützt, wird das **Value-Element** für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH festgelegt. 
  
Um zu überprüfen, ob es sich bei einem PST um eine SharePoint PST handelt, stellen Sie das PST mit [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)bereit und rufen Sie dann **GetProps** für das Nachrichtenspeicherobjekt auf, das diese Eigenschaft anfordert. Wenn es vorhanden ist, können Sie davon ausgehen, dass das PST für SharePoint konfiguriert wurde. wenn nicht, wurde das PST nicht als SharePoint PST konfiguriert. 
  
Weitere Informationen zur Verwendung von **GetProps** für den Zugriff auf Eigenschaften finden Sie unter [Abrufen von MAPI-Eigenschaften.](retrieving-mapi-properties.md)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI verwendet die **IMAPIProp::GetProps-Methode,** um alle Eigenschaften für ein Objekt abzurufen, indem entweder NULL oder das Array übergeben wird, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) im  _lpPropTagArray-Parameter_ zurückgegeben wird.  <br/> |
   
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
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

