---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8df25eade1065adc198bc356ffa4c96434de0b18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595763"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine [IMAPIFormMgr-Schnittstelle](imapiformmgriunknown.md) für ein Formularbibliotheksanbieterobjekt im Kontext einer vorhandenen Sitzung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a>Parameter

 _pSession_
  
> [in] Zeiger auf die von der Clientanwendung verwendete Sitzung.
    
 _ppmgr_
  
> [out] Zeiger auf die zurückgegebene **IMAPIFormMgr-Schnittstelle.** 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem eine Clientanwendung die **MAPIOpenFormMgr-Funktion** aufgerufen hat, finden die meisten nachfolgenden formularbezogenen Interaktionen über den Formularbibliotheksanbieter oder eine vom Formularbibliotheksanbieter zurückgegebene Schnittstelle statt. Die **IMAPIFormMgr-Schnittstelle** ermöglicht es dem Client, mit Nachrichtenhandlern zu arbeiten und Auflösungen zwischen Nachrichtenklassen und Formularbibliotheken auszuführen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp öffnet den Formular-Manager, damit ein Formular ausgewählt werden kann.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI verwendet die **MAPIOpenFormMgr-Methode,** um den Formular-Manager zu öffnen, damit ein Formular ausgewählt werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

