---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 91c78852092e6f6de9d64574e0b8369a63f6d3a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596316"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert an, dass das Formular alle Aufgaben ausführt, die es einem bestimmten Verb zuweist.
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>Parameter

 _iVerb_
  
> [in] Die Nummer, die einem der Verben des Formulars zugeordnet ist.
    
 _lpViewContext_
  
> [in] Ein Zeiger auf ein Ansichtskontextobjekt. Der  _lpViewContext-Parameter_ kann **NULL** sein.
    
 _hwndParent_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden. Der  _Parameter hwndParent_ sollte **null** sein, wenn das Dialogfeld oder Fenster nicht modal ist. 
    
 _lprcPosRect_
  
> [in] Ein Zeiger auf eine [Win32-RECT-Struktur,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) die die Größe und Position des Formularfensters enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Verb wurde erfolgreich aufgerufen.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Das vom  _iVerb-Parameter_ dargestellte Verb ist gültig, aber das Formular kann nicht die vorgänge ausführen, die ihm derzeit zugeordnet sind. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularviewer rufen die **IMAPIForm::D oVerb-Methode** auf, um anzufordern, dass das Formular die Aufgaben ausführt, die es jedem verb zuweist, das das Formular unterstützt. 
  
Jedes der unterstützten Verben wird durch einen numerischen Wert identifiziert, der im **iVerb-Parameter** an  _DoVerb_ übergeben wird. Typische Implementierungen von **DoVerb** enthalten eine **Switch-Anweisung,** die die Werte testet, die für den  _iVerb-Parameter_ für das Formular gültig sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn die Formularanzeige einen Ansichtskontext im  _lpViewContext-Parameter_ angibt, verwenden Sie ihn in ihrer **DoVerb-Implementierung** anstelle des Ansichtskontexts, der in einem früheren Aufruf der [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) übergeben wurde. Nehmen Sie alle erforderlichen Änderungen an Ihren internen Datenstrukturen vor, und speichern Sie den Ansichtskontext nicht. 
  
Führen Sie die folgenden Aufgaben in Ihrer **DoVerb-Implementierung aus:** 
  
- Führen Sie den Code aus, der für das bestimmte Verb erforderlich ist, das dem  _iVerb-Parameter_ zugeordnet ist. 
    
- Stellen Sie ggf. den ursprünglichen Ansichtskontext wieder her.
    
- Wenn eine unbekannte Verbnummer übergeben wurde, geben Sie MAPI_E_NO_SUPPORT zurück. Andernfalls wird ein Ergebnis basierend auf dem Erfolg oder Fehler eines verbs zurückgegeben, das ausgeführt wurde.
    
- Schließen Sie das Formular. Es liegt immer in Ihrer Verantwortung, das Formular zu schließen, nachdem ein **DoVerb-Aufruf** abgeschlossen wurde. 
    
Einige Verben, z. B. Print, sollten in Bezug auf den **DoVerb-Aufruf** modal sein, d. h., der angegebene Vorgang muss abgeschlossen sein, bevor der **DoVerb-Aufruf** zurückgegeben wird. 
  
Rufen Sie die [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf, um die **rect-Struktur** abzurufen, die vom Fenster eines Formulars verwendet wird. 
  
Speichern Sie das Handle nicht im  _hwndParent-Parameter,_ da es, obwohl es in der Regel bis zum Abschluss von **DoVerb** gültig bleibt, sofort nach der Rückgabe des Aufrufs zerstört werden kann.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können nicht modale Verben als modale Verben verwenden, indem Sie  _lpViewContext_ auf eine Ansichtskontextimplementierung verweisen, die das VCSTATUS_MODAL-Flag aus der [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) zurückgibt. 
  
Weitere Informationen zu Verben in MAPI finden Sie unter [Form Verbs](form-verbs.md). Weitere Informationen dazu, wie Verben in OLE behandelt werden, finden Sie unter [OLE und Datenübertragung.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI verwendet die **IMAPIForm::D oVerb-Methode,** um ein Verb auf einem Formular aufzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Formularverben](form-verbs.md)

