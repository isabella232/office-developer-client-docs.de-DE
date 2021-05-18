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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412457"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Eigenschaftswert einer oder mehrere Eigenschaften eines Objekts ab.
  
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
  
> [in] Ein Zeiger auf ein Array von Eigenschaftstags, die die Eigenschaften identifizieren, deren Werte abgerufen werden sollen. Der  _lpPropTagArray-Parameter_ muss entweder NULL sein, der angibt, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden sollen, oder auf eine [SPropTagArray-Struktur](sproptagarray.md) verweisen, die ein oder mehrere Eigenschaftstags enthält. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die das Format für Eigenschaften angibt, deren Typ PT_UNSPECIFIED. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgenwerte für diese Eigenschaften sollten im Unicode-Format zurückgegeben werden. Wenn das MAPI_UNICODE nicht festgelegt ist, sollten die Zeichenfolgenwerte im ANSI-Format zurückgegeben werden.
    
 _lpcValues_
  
> [out] Ein Zeiger auf eine Anzahl von Eigenschaftswerten, auf die der  _lppPropArray-Parameter_ verweist. Wenn  _lppPropArray_ NULL ist, ist der Inhalt des  _lpcValues-Parameters_ null. 
    
 _lppPropArray_
  
> [out] Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaftswerte wurden erfolgreich abgerufen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber auf eine oder mehrere Eigenschaften konnte nicht zugegriffen werden. Das **aulPropTag-Element** des Eigenschaftswerts für jede nicht verfügbare Eigenschaft hat den Eigenschaftstyp PT_ERROR und den Bezeichner Null. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Null wurde im **cValues-Element** der **SPropTagArray-Struktur** übergeben, auf das _lpPropTagArray verweist._
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::GetProps-Methode** ruft die Eigenschaftswerte einer oder mehreren Eigenschaften eines Objekts ab. 
  
Die Eigenschaftswerte werden in der reihenfolge zurückgegeben, in der sie angefordert wurden (d. h. die Reihenfolge der Eigenschaften im Eigenschaftentagarray, auf die  _von lpPropTagArray_ verwiesen wird, entspricht der Reihenfolge im Array der Eigenschaftenwertstrukturen, auf die von  _lppPropArray_ verwiesen wird). 
  
Die in den **aulPropTag-Membern** des Eigenschaftstagarrays angegebenen Eigenschaftstypen geben den Werttyp an, der im **Value-Element** jeder Eigenschaftswertstruktur zurückgegeben werden soll. Wenn der Aufrufer jedoch den Typ einer Eigenschaft nicht kennt, kann der Typ im **aulPropTag-Element** stattdessen auf PT_UNSPECIFIED. Beim Abrufen des **Werts legt GetProps** den richtigen Typ im **aulPropTag-Element** der Eigenschaftswertstruktur für die Eigenschaft fest. 
  
Wenn Eigenschaftstypen im **SPropTagArray** in _lpPropTagArray_ angegeben werden, verfügen die Eigenschaftswerte in der in _lppPropArray_ zurückgegebenen **SPropValue-Eigenschaft** über Typen, die exakt mit den angeforderten Typen übereinstimmen, es sei denn, stattdessen wird ein Fehlerwert zurückgegeben. 
  
Zeichenfolgeneigenschaften können einen von zwei Eigenschaftstypen aufweisen: PT_UNICODE, um das Unicode-Format und PT_STRING8 an das ANSI-Format zu stellen. Wenn das MAPI_UNICODE im  _ulFlags-Parameter_ festgelegt ist, gibt GetProps immer dann seinen Wert im Unicode-Format zurück, wenn **GetProps** das entsprechende Format für eine Zeichenfolgeneigenschaft nicht bestimmen kann. **GetProps kann** in den folgenden Situationen keinen genauen Zeichenfolgeneigenschaftentyp bestimmen: 
  
- Der  _lpPropTagArray-Parameter_ ist auf NULL festgelegt, um alle Eigenschaften an fordern. 
    
- Das **Element aulPropTag** enthält den Wert PT_UNSPECIFIED eigenschaftstyp im Eigenschaftentagarray. 
    
Wenn der  _lpPropTagArray-Parameter_ auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen und keine Eigenschaften vorhanden sind, führt **GetProps** die folgenden Schritte aus: 
  
- Gibt S_OK.
    
- Legt den Count-Wert im **cValues-Element** der Eigenschaftswertstruktur auf 0 fest. 
    
- Legt den Inhalt von  _lpcValues auf_ 0 fest. 
    
- Legt  _lppPropArray auf_ NULL fest. 
    
 **GetProps** darf keine Mehrwerteigenschaften zurückgeben, **wenn cValues** auf 0 festgelegt ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) auf, um zunächst Arbeitsspeicher für die [SPropValue-Struktur](spropvalue.md) zu reservieren, auf die  _von lpPropTagArray verwiesen wird._ rufen [Sie MAPIAllocateMore auf,](mapiallocatemore.md) um zusätzlichen Arbeitsspeicher zuzuordnen, der für die Mitglieder der Struktur erforderlich ist. 
  
Geben MAPI_W_ERRORS_RETURNED zurück, wenn Sie den Wert für eine oder mehrere der angeforderten Eigenschaften nicht abrufen können. Legen Sie in der Eigenschaftswertstruktur den Typ im **Element aulPropTag** auf PT_ERROR und value auf einen Statuscode fest, der den Fehler beschreibt.  Wenn Sie beispielsweise eine Zeichenfolge in Unicode konvertieren müssen und Unicode nicht unterstützen, legen Sie das **Value-Element** auf MAPI_E_BAD_CHARWIDTH. Wenn die Eigenschaft zu groß ist, legen Sie sie auf MAPI_E_NOT_ENOUGH_MEMORY. Wenn das Objekt die Eigenschaft nicht unterstützt, legen Sie sie auf MAPI_E_NOT_FOUND. 
  
Die Implementierung der **GetProps-Methode** durch einen Remotetransportanbieter muss die Eigenschaftswerte des Ordners für vom Aufrufer angeforderte Eigenschaften zurückgeben. Ihre Implementierung muss die folgenden Schritte unternehmen: 
  
- Weisen Sie ein Eigenschaftenwertarray zu, um an den Aufrufer zurückzukehren und dessen Adresse im Eigenschaftswertzeigerparameter zu speichern, der zu diesem Zweck übergeben wurde.
    
- Kopieren Sie die Eigenschaftstags aus den Eigenschaften des Ordners in die Eigenschaftstags im Eigenschaftswertarray entsprechend dem Array der Eigenschaftstags, die an **GetProps übergeben werden.**
    
- Stellen Sie sicher, dass der Eigenschaftentyp für alle Eigenschaftstags festgelegt ist, die an **GetProps übergeben werden.** Der Aufrufer kann einen Eigenschaftentyp von PT_UNSPECIFIED übergeben, in diesem Fall **muss GetProps** den richtigen Eigenschaftentyp für dieses Eigenschaftstag festlegen. 
    
- Legen Sie den Wert der einzelnen Eigenschaften im Eigenschaftswertarray entsprechend ihrem Tag. Wenn das vom Aufrufer angeforderte Eigenschaftstag beispielsweise PR_OBJECT_TYPE **(** [PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist, kann **GetProps** den Wert auf MAPI_FOLDER. 
    
- Wenn der Aufrufer eigenschaftstags übergibt, die ihre Implementierung nicht verarbeiten kann, können Sie das Eigenschaftstag auf PT_ERROR für diese Eigenschaften festlegen und den Eigenschaftswert auf MAPI_E_NOT_FOUND.
    
- Geben S_OK zurück, wenn keine Fehler aufgetreten sind, oder MAPI_W_ERRORS_RETURNED, wenn Fehler aufgetreten sind.
    
Die Implementierung der **GetProps-Methode** eines Remotetransportanbieters muss mindestens die folgenden Eigenschaften unterstützen: 
  
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

Rufen Sie für Eigenschaften vom Typ PT_OBJECT [die IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) anstelle von **GetProps auf.** 
  
Für sichere Eigenschaften sollten Sie sie nicht abrufen, indem Sie **GetProps** aufrufen, wenn der  _lppPropTagArray-Parameter_ auf NULL festgelegt ist. Sie müssen den Bezeichner einer sicheren Eigenschaft explizit im **aulPropTag-Element** des Eigenschaftentagarrays festlegen, wenn Sie **GetProps aufrufen.** Wann und wie eine sichere Eigenschaft verfügbar ist, liegt beim Dienstanbieter. 
  
Geben Sie die **zurückgegebene SPropValue-Struktur** frei, indem Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) nur aufrufen, wenn **GetProps** S_OK oder MAPI_W_ERRORS_RETURNED. 
  
Wenn **GetProps** MAPI_W_ERRORS_RETURNED, da er nicht auf eine oder mehrere Eigenschaften zugreifen konnte, überprüfen Sie die Eigenschaftstags der zurückgegebenen Eigenschaften. Für die fehlgeschlagenen Eigenschaften werden die folgenden Werte in ihrer Eigenschaftswertstruktur festgelegt: 
  
- Der Eigenschaftstyp im **Element aulPropTag,** das auf PT_ERROR. 
    
- Der Eigenschaftswert im **Value-Element** wird auf einen Statuscode für den Fehler festgelegt, z. B. MAPI_E_NOT_FOUND. 
    
Eigenschaften, die fehlschlagen, weil sie zu groß sind, um bequem in der Eigenschaftswertstruktur zurückgegeben zu werden, haben ihren **Value-Member** auf MAPI_E_NOT_ENOUGH_MEMORY. In der Regel tritt dies bei Zeichenfolgen- oder binären Eigenschaften des Typs PT_STRING8, PT_UNICODE oder PT_BINARY auf, wenn der Wert der Eigenschaft 4 KB oder größer ist. Rufen **Sie IMAPIProp::OpenProperty auf,** um große Eigenschaften abzurufen. 
  
Nicht alle Implementierungen von **GetProps** unterstützen sowohl die Unicode- als auch die ANSI-Formate für Zeichenzeichenfolgen. Wenn eine bestimmte Eigenschaft eine Zeichenfolgenformatkonvertierung erfordert und **GetProps** sie nicht unterstützt, wird das **Value-Element** für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH. 
  
Um zu überprüfen, ob es sich bei einer PST SharePoint pst handelt, stellen Sie die PST mithilfe von [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)ein, und rufen Sie **dann GetProps** für das Nachrichtenspeicherobjekt auf, das diese Eigenschaft anfordert. Wenn sie vorhanden ist, können Sie davon ausgehen, dass die #A0 für die SharePoint. Andern falls nicht, wurde das PST nicht als SharePoint konfiguriert. 
  
Weitere Informationen zur Verwendung von **GetProps** für den Zugriff auf Eigenschaften finden Sie unter [Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI verwendet die **IMAPIProp::GetProps-Methode,** um alle Eigenschaften für ein Objekt zu erhalten, indem null oder das array übergeben wird, das von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) im  _lpPropTagArray-Parameter_ zurückgegeben wird.  <br/> |
   
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

