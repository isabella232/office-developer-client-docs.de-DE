---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fdd5d01b96c9ea756ee64f113ccb5119a9693668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594467"
---
# <a name="servicewizarddlgproc"></a>SERVICEWIZARDDLGPROC
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert eine Callback-Funktion aufgerufen, die vom Assistenten Profil zu einem Dienstanbieter reagieren auf Benutzerereignisse, wenn der Anbieters Eigenschaftenseiten oder Seiten angezeigt werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI-Profil-Assistent  <br/> |
   
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
  
> [in] Fensterhandle an, das Dialogfeld-Profil-Assistent. 
    
_wMsgID_
  
> [in] Die Fensternachricht im verarbeitet werden. Zusätzlich zu den regulären Fenster-Nachrichten von einem modalen Dialogfeld erwartet können die folgenden Nachrichten empfangen werden:
    
WM_CLOSE 
  
> Der Profil-Assistent wurde abgeschlossen. Der Dienstanbieter sollten alle Bereinigung tun, wie Speicher Aufheben der Zuweisung von einem dynamisch zugewiesen werden. 
    
WM_COMMAND 
  
> Eines der Steuerelemente des Anbieters ausgewählt wurde, oder die **nächsten** oder **zurück** -Schaltfläche geklickt hat. Der Wert in der _wParam_ -Parameter gibt an, welches dieser Benutzerereignisse eingetreten ist. 
    
WM_INITDIALOG 
  
> Der Benutzer wurde an eine andere Eigenschaftenseite verschoben, für die das Dialogfeld initialisiert werden muss. Der Anbieter sollte die Steuerelemente initialisieren, die der Profil-Assistent zum Dialogfeld hinzugefügt hat. 
    
WIZ_QUERYNUMPAGES 
  
> Der Profil-Assistent ist für die Anzahl der Seiten aufgefordert werden, die zum Anzeigen der Anbieter benötigt. Der Anbieter sollte die Anzahl der Seiten anstelle von TRUE oder FALSE zurückgegeben. Verwenden Sie beispielsweise die folgenden return-Anweisung um anzugeben, dass drei Seiten angezeigt werden soll:
    
   ```cpp
return (BOOL)3;

   ```

_wParam_
  
> [in] Ein 32-Bit-Parameter Fenster-Nachrichten zugeordnet. Mögliche Werte hängen von der in der _wMsgID_ -Parameter angegebenen Nachricht ab. Zusätzlich zu den Werten, die mit den normalen Fenster-Nachrichten für ein modales Dialogfeld erwartet können die folgenden Werte erhalten: 
    
WIZ_NEXT 
  
> Wenn _wMsgID_ WM_COMMAND enthält, hat der Benutzer die Schaltfläche **Weiter** geklickt hat. 
    
WIZ_PREV 
  
> Wenn _wMsgID_ WM_COMMAND enthält, hat der Benutzer durch Klicken auf die Schaltfläche **zurück** . 
    
_lParam_
  
> [in] Ein 32-Bit-Parameter Fenster-Nachrichten zugeordnet. Mögliche Werte hängen von der in der _wMsgID_ -Parameter angegebenen Nachricht ab. 
    
## <a name="return-value"></a>R�ckgabewert

Der von einer **SERVICEWIZARDDLGPROC** Basis-Funktion zurückgegebene Wert ist die empfangene Meldung Fenster abhängig. Beachten Sie insbesondere, dass die außergewöhnliche Wert für die Nachricht WIZ_QUERYNUMPAGES zurückzugeben. Normale zurückgegebenen Werte sind: 
  
TRUE 
  
> Der Dienstanbieter hat die empfangene Meldung verarbeitet. 
    
FALSE 
  
> Der Dienstanbieter noch die empfangene Meldung nicht verarbeitet werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Benutzer eine Eigenschaft auf der Seite zu einer anderen bewegt wird, ist der Anbieter für die alte Seite Steuerelemente ein- und Ausblenden von den Steuerelementen zum nächsten oder vorherigen Seite verantwortlich. Wenn der Benutzer auf die Schaltfläche **Weiter** klickt, wird die **SERVICEWIZARDDLGPROC** Basis-Funktion mit der WM_COMMAND-Meldung und WIZ_NEXT im _wParam_ -Parameter aufgerufen. Die folgenden Schritte beschreiben, was geschieht, zwischen dem Zeitpunkt der Benutzer **Weiter** klickt und Zeitpunkt, zu dem der erste Anbieter Konfigurationsseiten gerendert werden. 
  
1. Der Profil-Assistent werden alle Steuerelemente, die auf das Fenster sind ausgeblendet. 
    
2. Der Profil-Assistent hinzugefügt die Seite des Anbieters ausgeblendete Steuerelemente. 
    
3. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**, senden die Nachricht WM_INITDIALOG, damit der Anbieter die Steuerelemente initialisieren kann. 
    
4. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**, die WIZ_QUERYNUMPAGES-Nachricht senden. Der Anbieter gibt die Anzahl der Seiten, die angezeigt werden sollen. 
    
5. Der Profil-Assistent ruft **SERVICEWIZARDDLGPROC**, senden die WM_COMMAND-Meldung mit dem _wParam_ -Parameter auf WIZ_NEXT oder WIZ_PREV festgelegt. Zu diesem Zeitpunkt der Anbieter entweder gibt FALSE {Fehler} zurück oder zeigt dessen Steuerelemente und gibt TRUE zurück {Erfolg}. Wenn der Profil-Assistent ID_NEXT übergibt, wird die erste Seite des Anbieters angezeigt. Wenn ID_PREV übergeben wird, wird die letzte Seite angezeigt. 
    
6. Der Profil-Assistent ruft der Anbieter **SERVICEWIZARDDLGPROC** Funktion senden die WM_COMMAND-Meldung mit dem _wParam_ -Parameter auf WIZ_NEXT oder WIZ_PREV (je nachdem, auf welche Schaltfläche der Benutzer geklickt hat) festgelegt. Der Anbieter ist verantwortlich für ein- oder Ausblenden von dessen Steuerelemente, und Schreiben von Daten in die **IMAPIProp** an der Profil-Assistent schrittweise durchlaufen ihrer Sequenz von Seiten übergeben. Der Anbieter sollte TRUE zurück, wenn die nächste oder der vorherige Seite wurde erfolgreich angezeigt werden soll, und FALSE, wenn weder der nächsten oder vorherigen Seite angezeigt werden konnten. Der Anbieter muss beachten, wenn sie außerhalb der Reihenfolge von Seiten Einzelschritt ist, und durch Ausblenden von dessen Steuerelemente und Schreiben von Daten auf das Profil entsprechend reagieren. 
    
7. Wenn der Benutzer außerhalb des Anbieters Seitenbereich Schritte, löscht den Anbieter ausgeblendete Steuerelemente im Dialogfeld der Profil-Assistent und ruft den nächsten Anbieter oder die nächste Seite angezeigt, wenn das letzte Anbieter war. 
    

