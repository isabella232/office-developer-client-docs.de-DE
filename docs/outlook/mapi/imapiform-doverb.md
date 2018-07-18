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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9ea44c9ba75390f06ff12ddeed0c7b652538e07d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792161"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Betrifft**: Outlook 
  
Fordert, dass das Formular ausführen, was es Aufgaben ein bestimmtes Verb zugeordnet.
  
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
  
> [in] Die Anzahl eines Verben für das Formular zugeordnet ist.
    
 _lpViewContext_
  
> [in] Ein Zeiger auf eine Ansicht Context-Objekt. Der Parameter _LpViewContext_ kann **null**sein.
    
 _hwndParent_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an. Der Parameter _HwndParent_ muss **null** sein, wenn das Dialogfeld oder Fenster nicht modalen Zustand befindet. 
    
 _lprcPosRect_
  
> [in] Ein Zeiger auf eine Win32- [Rechteck](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) -Struktur, die die Größe und Position des Fenster des Formulars enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Verb wurde erfolgreich aufgerufen.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> Das Verb, dargestellt durch den Parameter _iVerb_ ist gültig, aber das Formular kann nicht ausgeführt werden die Vorgänge, die derzeit zugeordnet. 
    
## <a name="remarks"></a>Bemerkungen

Formular Viewer rufen Sie die **IMAPIForm::DoVerb** -Methode, um anzufordern, dass das Formular der Aufgaben, bei denen es jedes Verb zugeordnet, die das Formular unterstützt. 
  
Jeder der unterstützten Verben wird durch einen numerischen Wert, der im Parameter _iVerb_ **DoVerb** übergeben identifiziert. Typische Implementierungen von **DoVerb** enthalten eine **switch** -Anweisung, die die Werte getestet, die für den Parameter _iVerb_ für das Formular gültig sind. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Verwenden sie der Formular-Viewer ein Ansichtskontext im _LpViewContext_ -Parameter gibt an, in der Implementierung **DoVerb** anstelle der Ansichtskontext einen früheren Aufruf der [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) -Methode übergeben. Stellen Sie alle Änderungen sind erforderlich, um Ihre internen Datenstrukturen und den Ansichtskontext nicht speichern. 
  
Führen Sie die folgenden Aufgaben in der Implementierung **DoVerb** : 
  
- Führen Sie den Code für das jeweilige Verb erforderlich ist, mit dem Parameter _iVerb_ verbunden ist. 
    
- Bei Bedarf wiederherstellen Sie den ursprünglichen Ansichtskontext.
    
- Wenn eine unbekannte Verbanzahl übergeben wurde, geben Sie MAPI_E_NO_SUPPORT zurück. Anderenfalls zurückgeben Sie basierend auf den Erfolg oder Misserfolg des jegliches Verb ausgeführt wurde.
    
- Schließen Sie das Formular. Es ist immer sicherstellen, dass Sie das Formular nach Abschluss einer **DoVerb** -Aufrufs zu schließen. 
    
Einige Verben, wie beispielsweise drucken, sollte im Hinblick auf den Anruf **DoVerb** modal sein – d. h., die angegebene Operation muss gestartet werden, bevor der Aufruf **DoVerb** beendet. 
  
Rufen Sie die [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) -Funktion, um die **Rechteck** -Struktur, die von einem Formular zugrunde Fenster verwendet zu erhalten. 
  
Speichern Sie das Handle nicht im Parameter _HwndParent_ , da es in der Regel gültig bis zum Abschluss des **DoVerb**bleibt, es sofort bei der Rückgabe des Aufrufs gelöscht werden kann.
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können festlegen, dass nicht gebundenes Verben fungieren als modales Verben zeigen Sie _LpViewContext_ an die Implementierung einer Ansicht Kontext, die die Kennzeichen VCSTATUS_MODAL von der [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) -Methode zurückgibt. 
  
Weitere Informationen zu Verben in MAPI finden Sie unter [Formular Verben](form-verbs.md). Weitere Informationen dazu, wie Verben in OLE behandelt werden finden Sie unter [OLE und Daten übertragen](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI (engl.) verwendet die **IMAPIForm::DoVerb** -Methode zum Aufrufen eines Verbs in einem Formular.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Formularverben](form-verbs.md)

