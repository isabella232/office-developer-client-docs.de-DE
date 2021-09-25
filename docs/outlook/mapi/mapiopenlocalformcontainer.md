---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4be35e9e337a4013023c1ab48138f104ea1b2842
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579461"
---
# <a name="mapiopenlocalformcontainer"></a>MAPIOpenLocalFormContainer

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Schnittstellenzeiger auf die lokale Formularbibliothek zurück. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a>Parameter

 _ppfcnt_
  
> [out] Zeiger auf einen Zeiger auf die schnittstelle der lokalen Formularbibliothek.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Schnittstelle, an die ein Zeiger zurückgegeben wird, kann von Installationsprogrammen von Drittanbietern verwendet werden, um anwendungsspezifische Formulare in der Bibliothek zu installieren, ohne dass sich das Programm zuerst bei der MAPI anmelden muss. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMaindlg::OnMAPIOpenLocalFormContainer  <br/> |MFCMAPI verwendet die **MAPIOpenLocalFormContainer-Methode,** um den lokalen Formularcontainer zum Rendern in einem neuen Fenster zu öffnen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

