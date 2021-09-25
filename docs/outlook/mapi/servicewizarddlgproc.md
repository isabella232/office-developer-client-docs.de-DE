---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ddc9b68bef81b02b3b9e0f8593cc937348566be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591164"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die vom Profil-Assistenten aufgerufen wird, damit ein Dienstanbieter auf Benutzerereignisse reagieren kann, wenn die Eigenschaftenblätter oder Seiten des Anbieters angezeigt werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI-Profil-Assistent  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a>Parameter

_hDlg_
  
> [in] Fensterhandle für das Dialogfeld "Profil-Assistent". 
    
_wMsgID_
  
> [in] Die zu verarbeitende Fenstermeldung. Zusätzlich zu den normalen Fenstermeldungen, die von einem modalen Dialogfeld erwartet werden, können die folgenden Nachrichten empfangen werden:
    
WM_CLOSE 
  
> Der Profil-Assistent wurde abgeschlossen. Der Dienstanbieter sollte alle erforderlichen Bereinigungen durchführen, z. B. die Zuordnung von dynamisch zugewiesenen Arbeitsspeichers. 
    
WM_COMMAND 
  
> Eines der Steuerelemente des Anbieters wurde ausgewählt oder auf die Schaltfläche **"Weiter"** oder **"Zurück"** geklickt. Der Wert im  _wParam-Parameter_ gibt an, welches dieser Benutzerereignisse aufgetreten ist. 
    
WM_INITDIALOG 
  
> Der Benutzer hat zu einer anderen Eigenschaftenseite gewechselt, für die das Dialogfeld initialisiert werden muss. Der Anbieter sollte die Steuerelemente initialisieren, die der Profil-Assistent dem Dialogfeld hinzugefügt hat. 
    
WIZ_QUERYNUMPAGES 
  
> Der Profil-Assistent fordert die Anzahl der Seiten an, die der Anbieter anzeigen muss. Der Anbieter sollte die Anzahl der Seiten anstelle von TRUE oder FALSE zurückgeben. Verwenden Sie beispielsweise die folgende Return-Anweisung, um anzugeben, dass drei Seiten angezeigt werden sollen:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Ein 32-Bit-Parameter, der Fenstermeldungen zugeordnet ist. Mögliche Werte hängen von der im  _wMsgID-Parameter_ angegebenen Nachricht ab. Zusätzlich zu den werten, die bei den regulären Fenstermeldungen für ein modales Dialogfeld erwartet werden, können die folgenden Werte empfangen werden: 
    
WIZ_NEXT 
  
> Wenn  _wMsgID_ WM_COMMAND enthält, hat der Benutzer auf die Schaltfläche **"Weiter"** geklickt. 
    
WIZ_PREV 
  
> Wenn  _wMsgID_ WM_COMMAND enthält, hat der Benutzer auf die Schaltfläche **"Zurück"** geklickt. 
    
_lParam_
  
> [in] Ein 32-Bit-Parameter, der Fenstermeldungen zugeordnet ist. Mögliche Werte hängen von der im  _wMsgID-Parameter_ angegebenen Nachricht ab. 
    
## <a name="return-value"></a>Rückgabewert

Der von einer **SERVICEWIZARDDLGPCROSS-basierten** Funktion zurückgegebene Wert hängt von der empfangenen Fensternachricht ab. Beachten Sie insbesondere den Ausnahmerückgabewert für die WIZ_QUERYNUMPAGES Nachricht. Die normalen Rückgabewerte sind: 
  
TRUE 
  
> Der Dienstanbieter hat die Nachricht des empfangenen Fensters verarbeitet. 
    
FALSE 
  
> Der Dienstanbieter hat die Nachricht des empfangenen Fensters nicht verarbeitet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Benutzer von einer Eigenschaftenseite zu einer anderen wechselt, ist der Anbieter dafür verantwortlich, die Steuerelemente der alten Seite zu verbergen und die Steuerelemente für die nächste oder vorherige Seite anzuzeigen. Wenn der Benutzer auf die Schaltfläche **"Weiter"** klickt, wird die **auf SERVICEWIZARDDLGP XAML** basierende Funktion mit der WM_COMMAND Nachricht und WIZ_NEXT im  _wParam-Parameter_ aufgerufen. In den folgenden Schritten wird beschrieben, was zwischen dem Klicken des Benutzers auf **"Weiter"** und dem Rendern der Konfigurationsseiten des ersten Anbieters geschieht. 
  
1. Der Profil-Assistent blendet alle Steuerelemente aus, die sich im Fenster befinden. 
    
2. Der Profil-Assistent fügt die ausgeblendeten Steuerelemente des Anbieters zur Seite hinzu. 
    
3. Der Profil-Assistent ruft **SERVICEWIZARDDLGP XAML** auf und sendet die WM_INITDIALOG Nachricht, damit der Anbieter die Steuerelemente initialisieren kann. 
    
4. Der Profil-Assistent ruft **SERVICEWIZARDDLGP XAML** auf und sendet die WIZ_QUERYNUMPAGES Nachricht. Der Anbieter gibt die Anzahl der Seiten zurück, die angezeigt werden sollen. 
    
5. Der Profil-Assistent ruft **SERVICEWIZARDDLGP XAML** auf und sendet die WM_COMMAND Nachricht, wobei der  _wParam-Parameter_ auf WIZ_NEXT oder WIZ_PREV festgelegt ist. An diesem Punkt gibt der Anbieter entweder FALSE {error} zurück oder zeigt seine Steuerelemente an und gibt TRUE {success} zurück. Wenn der Profil-Assistent ID_NEXT übergibt, wird die erste Seite des Anbieters angezeigt. Wenn ID_PREV übergeben wird, wird die letzte Seite angezeigt. 
    
6. Der Profil-Assistent ruft die **SERVICEWIZARDDLGPCROSS-Funktion** des Anbieters auf und sendet die WM_COMMAND Nachricht, wobei der  _wParam-Parameter_ auf WIZ_NEXT oder WIZ_PREV festgelegt ist (je nachdem, auf welche Schaltfläche der Benutzer geklickt hat). Der Anbieter ist dafür verantwortlich, seine Steuerelemente anzuzeigen oder zu verbergen und seine Daten in die AN den Profil-Assistenten übergebene **IMAPIProp** zu schreiben, um die Abfolge der Seiten zu durchlaufen. Der Anbieter sollte TRUE zurückgeben, wenn die nächste oder vorherige Seite erfolgreich angezeigt wurde, und FALSE, wenn weder die nächste noch die vorherige Seite angezeigt werden konnte. Der Anbieter muss sich bewusst sein, wenn er außerhalb seiner Abfolge von Seiten wechselt, und entsprechend reagieren, indem er seine Steuerelemente ausblendet und seine Daten in das Profil schreibt. 
    
7. Wenn der Benutzer schritte außerhalb des Seitenbereichs des Anbieters ausführt, löscht der Profil-Assistent die ausgeblendeten Steuerelemente des Anbieters aus dem Dialogfeld und ruft den nächsten Anbieter auf oder zeigt die nächste Seite an, wenn dies der letzte Anbieter war. 
    

