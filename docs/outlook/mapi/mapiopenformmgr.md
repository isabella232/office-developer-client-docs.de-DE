---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 592bd2c88c8eea17d80fe7cb725b075235c51763
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793128"
---
# <a name="mapiopenformmgr"></a>MAPIOpenFormMgr

  
  
**Betrifft**: Outlook 
  
Öffnet eine [IMAPIFormMgr](imapiformmgriunknown.md) -Schnittstelle in einem Formular Bibliothek Anbieter-Objekt im Zusammenhang mit einer vorhandenen Sitzung an. 
  
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
  
> [in] Zeiger auf die Sitzung von der Clientanwendung verwendet.
    
 _ppmgr_
  
> [out] Zeiger auf die zurückgegebene Schnittstelle **IMAPIFormMgr** . 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Bemerkungen

Nach eine Clientanwendung an die **MAPIOpenFormMgr** -Funktion aufruft, erfolgen die meisten nachfolgende Forms-bezogene Interaktionen über den Formular-Bibliothek-Anbieter oder eine Schnittstelle, die vom Formular Bibliotheksanbieter zurückgegeben. Die **IMAPIFormMgr** -Schnittstelle ermöglicht dem Client zum Arbeiten mit Message Handler und Ausführen von Lösungen zwischen Nachrichtenklassen und Formularbibliotheken. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp öffnet den Formular-Manager aus, damit ein Formular ausgewählt werden kann.  <br/> |CMainDlg::OnSelectForm  <br/> |MFCMAPI (engl.) verwendet die **MAPIOpenFormMgr** -Methode, um den Formular-Manager zu öffnen, damit ein Formular ausgewählt werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

