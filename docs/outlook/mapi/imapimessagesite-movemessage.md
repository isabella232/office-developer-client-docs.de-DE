---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2efdf723e38f45c13d53467dd67100b883ed8944
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575967"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Verschiebt die aktuelle Nachricht in einen Ordner.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameter

 _pFolderDestination_
  
> [in] Ein Zeiger auf den Ordner, in den die Nachricht verschoben werden soll.
    
 _pViewContext_
  
> [in] Ein Zeiger auf ein Ansichtskontextobjekt.
    
 _prcPosRect_
  
> [in] Ein Zeiger auf eine [RECT-Struktur,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) die die Fenstergröße und -position des aktuellen Formulars enthält. Das nächste angezeigte Formular verwendet auch dieses Fensterrechteck. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NO_SUPPORT 
  
> Der Vorgang wird von dieser Nachrichtenwebsite nicht unterstützt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Formularobjekte rufen die **IMAPIMessageSite::MoveMessage-Methode** auf, um die aktuelle Nachricht in einen neuen Ordner zu verschieben. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **MoveMessage-Implementierung** eines Formularviewers muss die [IMAPIViewContext::ActivateNext-Methode](imapiviewcontext-activatenext.md) aufrufen und das flag VCDIR_MOVE übergeben, bevor die Nachricht tatsächlich in einen neuen Ordner verschoben wird. Rufen Sie die Windows [GetWindowRect-Funktion](https://msdn.microsoft.com/library/ms633519) auf, um die von einem Formularfenster verwendete **RECT-Struktur** abzurufen. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI-Formularschnittstellen.](mapi-form-interfaces.md)
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Nach der Rückgabe von **MoveMessage** müssen Formulare nach einer aktuellen Nachricht suchen und sich dann selbst schließen, wenn keine vorhanden ist. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Nicht implementiert.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

