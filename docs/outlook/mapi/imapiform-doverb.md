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
  
Fordert an, dass das Formular alle Aufgaben ausführen soll, die es einem bestimmten Verb zurrent.
  
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
  
> [in] Die Zahl, die einem der Verben des Formulars zugeordnet ist.
    
 _lpViewContext_
  
> [in] Ein Zeiger auf ein Ansichtskontextobjekt. Der _lpViewContext-Parameter_ kann **null sein.**
    
 _hwndParent_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt. Der  _hwndParent-Parameter_ sollte **null sein,** wenn das Dialogfeld oder Fenster nicht modal ist. 
    
 _lprcPosRect_
  
> [in] Ein Zeiger auf eine Win32 [RECT-Struktur,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) die die Größe und Position des Formularfensters enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Verb wurde erfolgreich aufgerufen.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Das verb, das durch den  _iVerb-Parameter_ dargestellt wird, ist gültig, aber das Formular kann die derzeit zugeordneten Vorgänge nicht ausführen. 
    
## <a name="remarks"></a>Hinweise

Formularbetrachter rufen die **IMAPIForm::D oVerb-Methode** auf, um anzusinnen, dass das Formular die Aufgaben ausführen soll, die es mit jedem verb verknüpft, das das Formular unterstützt. 
  
Jedes der unterstützten Verben wird durch einen numerischen Wert identifiziert, der im **iVerb-Parameter** an  _DoVerb übergeben_ wird. Typische Implementierungen von **DoVerb** enthalten eine **switch-Anweisung,** die die Werte testet, die für den  _iVerb-Parameter_ für das Formular gültig sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn der Formularanzeiger einen Ansichtskontext im  _lpViewContext-Parameter_ angibt, verwenden Sie ihn in Der **DoVerb-Implementierung** anstelle des Ansichtskontexts, der in einem früheren Aufruf der [IMAPIForm::SetViewContext-Methode](imapiform-setviewcontext.md) übergeben wurde. Nehmen Sie alle änderungen vor, die an Ihren internen Datenstrukturen erforderlich sind, und speichern Sie den Ansichtskontext nicht. 
  
Führen Sie die folgenden Aufgaben in Ihrer **DoVerb-Implementierung** aus: 
  
- Führen Sie den code aus, der für das bestimmte Verb erforderlich ist, das dem  _iVerb-Parameter zugeordnet_ ist. 
    
- Stellen Sie bei Bedarf den ursprünglichen Ansichtskontext wieder auf.
    
- Wenn eine unbekannte Verbnummer übergeben wurde, geben Sie MAPI_E_NO_SUPPORT. Andernfalls geben Sie ein Ergebnis basierend auf dem Erfolg oder Fehler des Verbs zurück, das ausgeführt wurde.
    
- Schließen Sie das Formular. Es liegt immer in Ihrer Verantwortung, das Formular nach Abschluss eines **DoVerb-Anrufs** zu schließen. 
    
Einige Verben, z. B. Print, sollten im Hinblick auf den **DoVerb-Aufruf** modal sein, d. h. der angegebene Vorgang muss abgeschlossen sein, bevor der **DoVerb-Aufruf** zurückgegeben wird. 
  
Rufen Sie die [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf, um die vom Formularfenster verwendete **RECT-Struktur** zu erhalten. 
  
Speichern Sie das Handle nicht im  _hwndParent-Parameter,_ da es zwar in der Regel bis zum Abschluss von **DoVerb** gültig bleibt, es aber sofort nach der Rückgabe des Anrufs zerstört werden kann.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können nicht modale Verben als modale Verben verwenden, indem Sie  _lpViewContext_ auf eine Ansichtskontextimplementierung verweisen, die das VCSTATUS_MODAL-Flag aus der [IMAPIViewContext::GetViewStatus-Methode](imapiviewcontext-getviewstatus.md) zurückgibt. 
  
Weitere Informationen zu Verben in MAPI finden Sie unter [Form Verbs](form-verbs.md). Weitere Informationen zum Umgang mit Verben in OLE finden Sie unter [OLE und Datenübertragung](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI verwendet die **IMAPIForm::D oVerb-Methode** zum Aufrufen eines Verbs in einem Formular.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Formularverben](form-verbs.md)

