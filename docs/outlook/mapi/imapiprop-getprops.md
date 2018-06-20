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
ms.openlocfilehash: 33351235db2a9a3f9d9b67f59e8356a0fa8abfa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792279"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Betrifft**: Outlook 
  
Ruft den Wert der Eigenschaft um, der eine oder mehrere Eigenschaften eines Objekts an.
  
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
  
> [in] Ein Zeiger auf ein Array von Eigenschaftentags, mit denen die Eigenschaften, deren Werte abgerufen werden sollen. Der Parameter _LpPropTagArray_ muss entweder NULL-Wert zurück, der angibt, dass Werte für alle Eigenschaften des Objekts zurückgegeben werden soll, oder zeigen Sie auf eine [SPropTagArray](sproptagarray.md) -Struktur, die einen oder mehrere Eigenschaftentags enthält. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die das Format für Eigenschaften angibt, die den Typ PT_UNSPECIFIED aufweisen. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgenwerte für diese Eigenschaften sollte das Unicode-Format zurückgegeben werden. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sollte die Zeichenfolgenwerte im ANSI-Format zurückgegeben.
    
 _lpcValues_
  
> [out] Ein Zeiger auf eine Anzahl von Eigenschaftswerten auf den durch den Parameter _LppPropArray_ verwiesen. Wenn _LppPropArray_ NULL ist, wird der Inhalt des Parameters _LpcValues_ 0 (null). 
    
 _lppPropArray_
  
> [out] Ein Zeiger auf einen Zeiger auf die abgerufenen Eigenschaftswerte.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eigenschaftswerte wurden erfolgreich abgerufen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaften konnte nicht zugegriffen werden. **AulPropTag** Mitglied der Eigenschaftswert für jeden nicht verfügbar-Eigenschaft hat einen Eigenschaftentyp PT_ERROR und eine Kennung von 0 (null). Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> 0 (null) wurde im **cValues** -Member der **SPropTagArray** -Struktur, die auf den _LpPropTagArray_übergeben.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::GetProps** -Methode ruft die Eigenschaftswerte der eine oder mehrere Eigenschaften eines Objekts. 
  
Die Eigenschaftswerte werden in der gleichen Reihenfolge zurückgegeben, wie angefordert wurden (d. h., die Reihenfolge der Eigenschaften im Array Tag-Eigenschaft auf den _LpPropTagArray_ entspricht der Reihenfolge, in dem Array der Eigenschaft Wert Strukturen auf den _LppPropArray _). 
  
Die in der **AulPropTag** Elemente von Arrays der Tag-Eigenschaft angegebene Eigenschaftentypen angeben des Typs des Werts, der in der Member **Wert** jeder Eigenschaft-Wert-Struktur zurückgegeben werden soll. Wenn der Anrufer nicht den Typ einer Eigenschaft bekannt ist, kann jedoch der Typ im **AulPropTag** -Member stattdessen auf PT_UNSPECIFIED festgelegt. In das Abrufen des Werts, legt **GetProps** den korrekten Typ in der **AulPropTag** Member der Eigenschaft Wert Struktur für die Eigenschaft. 
  
Eigenschaftentypen in der **SPropTagArray** in _LpPropTagArray_angegeben, haben der Eigenschaftswerte in den **SPropValue** im _LppPropArray_ zurückgegebenen Typen, die die angeforderten Typen exakt übereinstimmen, sofern Sie kein Fehlerwert zurückgegeben wird Stattdessen. 
  
Zeichenfolgeneigenschaften können einen der beiden Typen aufweisen: PT_UNICODE PT_STRING8 zur Darstellung von ANSI-Format und die Unicode-Format dargestellt. Wenn die Option MAPI_UNICODE im Parameter _UlFlags_ festgelegt ist, wenn nicht das entsprechende Format für eine Zeichenfolgeneigenschaft **GetProps** bestimmen kann, wird den Wert in das Unicode-Format zurückgegeben. Eine exakte Zeichenfolge Eigenschaftentyp in den folgenden Situationen kann nicht **GetProps** ermitteln: 
  
- Der Parameter _LpPropTagArray_ ist auf NULL festgelegt, so fordern Sie alle Eigenschaften an. 
    
- Das **AulPropTag** -Element enthält den Wert PT_UNSPECIFIED als Eigenschaftentyp in Array der Tag-Eigenschaft. 
    
Wenn der _LpPropTagArray_ -Parameter auf NULL festgelegt ist, um alle Eigenschaften des Objekts abzurufen und keine Eigenschaften vorhanden, führt **GetProps** Folgendes aus: 
  
- Gibt S_OK zurück.
    
- Der Count-Wert festgelegt im **cValues** -Member der Eigenschaft Wert Struktur auf 0. 
    
- Der Inhalt des _LpcValues_ festgelegt auf 0. 
    
- _LppPropArray_ festgelegt auf NULL. 
    
 **GetProps** müssen keine zurück, dass Eigenschaften mit mehreren Werten mit **cValues** auf 0 festgelegt. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Rufen Sie die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, um Speicher ursprünglich für die [SPropValue](spropvalue.md) -Struktur, die auf den _LpPropTagArray_; Rufen Sie [MAPIAllocateMore](mapiallocatemore.md) zum Reservieren alle zusätzlichen Speichers für die Struktur Elemente erforderlich ist. 
  
Zurückgeben Sie MAPI_W_ERRORS_RETURNED, wenn Sie den Wert für eine oder mehrere der angeforderten Eigenschaften abrufen können. Legen Sie den Typ der Eigenschaft Wert Struktur in der Member **AulPropTag** PT_ERROR und der **Wert** Member einen Statuscode, der den Fehler beschreibt. Beispielsweise wenn Sie eine Zeichenfolge in Unicode konvertieren und Unicode nicht unterstützt, legen Sie den **Wert** Member auf MAPI_E_BAD_CHARWIDTH. Wenn die Eigenschaft zu groß ist, legen Sie es auf MAPI_E_NOT_ENOUGH_MEMORY. Wenn das Objekt die-Eigenschaft nicht unterstützt, festlegen Sie jedoch auf MAPI_E_NOT_FOUND. 
  
Implementierung der **GetProps** -Methode eines remote-Transport-Anbieters muss den Ordner Eigenschaftswerte für Eigenschaften, die vom Anrufer angefordert zurückgeben. Die Implementierung muss die folgenden Schritte ausführen: 
  
- Reservieren Sie eine Eigenschaft Wertearray, um an den Anrufer zurückgeben, und speichern Sie die Adresse in der Eigenschaft Value Zeiger-Parameter für diesen Zweck bestimmten übergeben.
    
- Kopieren Sie die Eigenschaftentags aus den Eigenschaften des Ordners, in die Eigenschaftentags im Array Eigenschaft Wert gemäß dem Array der Eigenschaftentags **GetProps**übergeben.
    
- Stellen Sie sicher, dass für alle Eigenschaftentags **GetProps**übergeben der Eigenschaftentyp festgelegt ist. Der Eigenschaftentyp PT_UNSPECIFIED, kann der Aufrufer übergeben in dem Fall **GetProps** den richtigen Eigenschaftstyp für diese Eigenschaftentag festgelegt werden muss. 
    
- Legen Sie den Wert jeder Eigenschaft im Array Eigenschaft Wert entsprechend der Tag. Angenommen, wenn das durch den Aufrufer angeforderte Eigenschafts-Tag **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) ist, können **GetProps** den Wert auf MAPI_FOLDER festgelegt. 
    
- Wenn der Aufrufer eine beliebige Eigenschaftentags, die die Implementierung nicht behandelt wird übergibt, können Sie das Eigenschafts-Tag auf PT_ERROR für diese Eigenschaften festgelegt und den Wert der Eigenschaft auf MAPI_E_NOT_FOUND festgelegt.
    
- Geben Sie S_OK zurück, wenn keine Fehler aufgetreten sind oder MAPI_W_ERRORS_RETURNED zurück, wenn Fehler aufgetreten sind.
    
Implementierung eines remote-Transport-Anbieters der **GetProps** -Methode muss mindestens die folgenden Eigenschaften unterstützen: 
  
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

Rufen Sie für Eigenschaften vom Typ PT_OBJECT die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode statt **GetProps**. 
  
Für sichere Eigenschaften davon ausgehen, dass sie abrufen durch Aufrufen von **GetProps** mit der _LppPropTagArray_ -Parameter auf NULL festgelegt wurde. Sie müssen beim Aufruf **GetProps**explizit eine sichere Eigenschaftenbezeichner im **AulPropTag** Mitglied des Arrays die Tag-Eigenschaft festlegen. Wann und wie eine sichere Eigenschaft verfügbar ist, wird bis zum Dienstanbieter. 
  
Frei die zurückgegebene Struktur **SPropValue** durch Aufrufen der Funktion [MAPIFreeBuffer](mapifreebuffer.md) nur, wenn **GetProps** S_OK oder MAPI_W_ERRORS_RETURNED zurückgibt. 
  
Wenn **GetProps** MAPI_W_ERRORS_RETURNED zurückgibt, da eine oder mehrere Eigenschaften nicht zugegriffen werden konnte, überprüfen Sie die Eigenschaftentags der zurückgegebenen Eigenschaften. Fehlgeschlagenen Eigenschaften müssen die folgenden Werte in die Struktur der Eigenschaft Wert festlegen: 
  
- Der Eigenschaftentyp im **AulPropTag** -Member auf PT_ERROR festgelegt. 
    
- Der Wert der Eigenschaft im Member **Wert** auf einen Statuscode des Fehlers, wie etwa MAPI_E_NOT_FOUND festgelegt. 
    
Eigenschaften, die nicht, da sie bequem in der Eigenschaft Wert Struktur zurückgegeben werden zu groß sind haben **ihre Element auf MAPI_E_NOT_ENOUGH_MEMORY festgelegt** . In der Regel Dies tritt auf, mit Zeichenfolgen oder binäre Eigenschaften vom Typ PT_STRING8, PT_UNICODE oder PT_BINARY Wenn der Wert der Eigenschaft 4 KB oder größer. Rufen Sie **IMAPIProp::OpenProperty** um große Eigenschaften abzurufen. 
  
Nicht alle Implementierungen von **GetProps** unterstützen die Unicode- und die ANSI-Formate für Zeichenfolgen. Wenn eine bestimmte Eigenschaft eine Zeichenfolge formatkonvertierung erforderlich und **GetProps** nicht wird unterstützt kann, wird der **Wert** Member für die Eigenschaft auf MAPI_E_BAD_CHARWIDTH festgelegt. 
  
Um zu überprüfen, ob eine PST-Datei auf einer SharePoint-PST-Datei ist, binden Sie die PST-Datei **GetProps** verwenden und [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), klicken Sie dann auf diese Eigenschaft anfordern Message Store-Objekts aufrufen. Wenn es vorhanden ist, können Sie davon ausgehen, dass die PST-Datei für SharePoint konfiguriert wurde; Wenn dies nicht der Fall ist, wird die PST-Datei als eine SharePoint-PST-Datei wurde nicht konfiguriert. 
  
Weitere Informationen zur Verwendung von **GetProps** für den Zugriff auf Eigenschaften, finden Sie unter [Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::GetProps** -Methode, um alle Eigenschaften für ein Objekt abrufen, indem Sie entweder NULL oder von der [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode im Parameter _LpPropTagArray_ zurückgegebenen Array übergeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp: IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Abrufen von MAPI-Eigenschaften](retrieving-mapi-properties.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

