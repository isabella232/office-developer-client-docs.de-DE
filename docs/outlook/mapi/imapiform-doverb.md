---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329460"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fordert an, dass das Formular alle Aufgaben ausführt, die es einem bestimmten Verb zuordnet.
  
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
  
> in Die Zahl, die einem der Verben des Formulars zugeordnet ist.
    
 _lpViewContext_
  
> in Ein Zeiger auf ein View-Kontextobjekt. Der _lpViewContext_ -Parameter kann **null**sein.
    
 _hwndParent_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, mit denen diese Methode angezeigt wird. Der _hwndParent_ -Parameter sollte **null** sein, wenn das Dialogfeld oder Fenster nicht modal ist. 
    
 _lprcPosRect_
  
> in Ein Zeiger auf eine Win32- [Rect](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) -Struktur, die die Größe und Position des Formularfensters enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Verb wurde erfolgreich aufgerufen.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Das Verb, das durch den _iVerb_ -Parameter dargestellt wird, ist gültig, aber das Formular kann die derzeit zugeordneten Vorgänge nicht ausführen. 
    
## <a name="remarks"></a>Hinweise

Formular Betrachter rufen die **IMAPIForm::D overb** -Methode auf, um anzufordern, dass das Formular die Aufgaben ausführt, die es jedem Verb zuordnet, das das Formular unterstützt. 
  
Jedes der unterstützten Verben wird durch einen numerischen Wert identifiziert, der im _iVerb_ -Parameter an **DoVerb** übergeben wird. Typische Implementierungen von **DoVerb** enthalten eine **Switch** -Anweisung, die die Werte testet, die für den _iVerb_ -Parameter für das Formular gültig sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Formular Anzeiger einen Ansichtskontext im _lpViewContext_ -Parameter angibt, verwenden Sie ihn in Ihrer **DoVerb** -Implementierung anstelle des in einem früheren Aufruf der [IMAPIForm::](imapiform-setviewcontext.md) setviewcontext-Methode übergebenen Ansichts Kontexts. Nehmen Sie alle erforderlichen Änderungen an Ihren internen Datenstrukturen vor, und speichern Sie den Ansichtskontext nicht. 
  
Führen Sie die folgenden Aufgaben in der **DoVerb** -Implementierung aus: 
  
- Führen Sie den Code aus, der für das jeweilige Verb erforderlich ist, das dem Parameter _iVerb_ zugeordnet ist. 
    
- Stellen Sie bei Bedarf den ursprünglichen Ansichtskontext wieder her.
    
- Wenn eine unbekannte Verb-Zahl übergeben wurde, geben Sie MAPI_E_NO_SUPPORT. Andernfalls wird ein Ergebnis basierend auf dem Erfolg oder Fehler des ausgeführten Verbs zurückgegeben.
    
- Schließen Sie das Formular. Es ist immer Ihre Aufgabe, das Formular zu schließen, nachdem ein **DoVerb** -Aufruf abgeschlossen wurde. 
    
Einige Verben, wie beispielsweise Print, sollten im Hinblick auf den **DoVerb** -Aufruf modal sein, d. h., der angegebene Vorgang muss abgeschlossen sein, bevor der **DoVerb** -Aufruf zurückgegeben wird. 
  
Rufen Sie die [GetWindowRect](https://msdn.microsoft.com/library/ms633519) -Funktion auf, um die vom Fenster eines Formulars verwendete **Rect** -Struktur zu erhalten. 
  
Speichern Sie das Handle nicht im Parameter _hwndParent_ , da es, obwohl es in der Regel bis zum Abschluss von **DoVerb**gültig bleibt, sofort nach der Rückgabe des Aufrufs zerstört werden kann.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können nicht modale Verben als modale Verben fungieren lassen, indem Sie _lpViewContext_ auf eine Kontext Implementierung zeigen, die das VCSTATUS_MODAL-Flag von der [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode zurückgibt. 
  
Weitere Informationen zu Verben in MAPI finden Sie unter [Formular Verben](form-verbs.md). Weitere Informationen dazu, wie Verben in OLE behandelt werden, finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MfcMapi verwendet die **IMAPIForm::D overb** -Methode, um ein Verb in einem Formular aufzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Formular Verben](form-verbs.md)

