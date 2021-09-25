---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e6f449728d985de1d263c25ee20239c64a4ad735
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556952"
---
# <a name="adrparm"></a>ADRPARM

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Anzeige und das Verhalten des allgemeinen Adressdialogfelds. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Members

**cbABContEntryID**
  
> Anzahl der Bytes im Eintragsbezeichner, auf die durch **lpABContEntryID** verwiesen wird.
    
**lpABContEntryID**
  
> Zeiger auf den Eintragsbezeichner des Containers, der die anfängliche Liste der Empfängeradressen bereitstellt, die im Adressdialogfeld angezeigt werden.
    
**ulFlags**
  
> Bitmaske von Flags, die verschiedenen Optionen des Adressdialogfelds zugeordnet sind. Die folgenden Flags können festgelegt werden:
    
AB_RESOLVE
  
> Aktivieren Sie, dass alle Namen aufgelöst werden, nachdem das Adressdialogfeld geschlossen wurde. Wenn es mehrdeutige Einträge gibt, die sich aus dem Prozess der Namensauflösung ergeben, wird der Benutzer in einem Dialogfeld aufgefordert, Hilfe bei der Auflösung dieser Einträge zu erhalten. Durch Festlegen dieses Kennzeichens wird sichergestellt, dass alle von [IAddrBook::Address zurückgegebenen](iaddrbook-address.md) Namen aufgelöst werden. 
    
AB_SELECTONLY
  
> Deaktivieren Sie die Erstellung von einmaligen Adressen für eine Empfängerliste. Dieses Kennzeichen wird nur verwendet, wenn das Dialogfeld modal ist, wie durch das festzulegende DIALOG_MODAL-Kennzeichen angegeben.
    
ADDRESS_ONE
  
> Der Benutzer kann genau einen Empfänger anstelle mehrerer Empfänger aus einer Liste auswählen. Dieses Kennzeichen ist nur gültig, wenn **cDestFields** null ist und das Dialogfeld modal ist, wie durch das DIALOG_MODAL festgelegt wird. 
    
DIALOG_MODAL
  
> Bewirkt, dass die modale Version des allgemeinen Adressdialogfelds angezeigt wird. Entweder dieses Flag oder DIALOG_SDI sollte festgelegt werden. sie können nicht beide festlegen. 
    
DIALOG_OPTIONS
  
> Bewirkt, dass die Schaltfläche **"Sendeoptionen"** im Dialogfeld angezeigt wird. Dieses Kennzeichen wird nur verwendet, wenn das Dialogfeld modal ist, wie durch das festzulegende DIALOG_MODAL-Kennzeichen angegeben. 
    
DIALOG_SDI
  
> Bewirkt, dass die moduslose Version des allgemeinen Adressdialogfelds angezeigt wird. Entweder dieses Flag oder DIALOG_MODAL sollte festgelegt werden. sie können nicht beide festlegen. Das flag DIALOG_SDI wird für Nicht-Outlook-Clients ignoriert, und die modale Version des Dialogfelds wird angezeigt. Daher sollte im  _Parameter lpulUIParam_ von [IAddrBook::Address](iaddrbook-address.md)kein Zeiger auf ein Handle erwartet werden.
    
**lpReserved**
  
> Reserviert, muss Null sein.
    
**ulHelpContext**
  
> Gibt den Kontext in der **Hilfe** an, der zuerst angezeigt wird, wenn der Benutzer im Adressdialogfeld auf die Schaltfläche "Hilfe" klickt. 
    
**lpszHelpFileName**
  
> Zeiger auf den Namen einer Hilfedatei, die dem Adressdialogfeld zugeordnet wird. Der **lpszHelpFileName-Member** wird zusammen mit **ulHelpContext** verwendet, um die Windows **WinHelp-Funktion** aufzurufen. 
    
**lpfnABSDI**
  
> Zeiger auf eine MAPI-Funktion basierend auf dem [ACCELERATEABSDI-Prototyp](accelerateabsdi.md) oder NULL. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das DIALOG_SDI-Kennzeichen angegeben wird. Clients, die eine **ADRPARM-Struktur** erstellen, die an [IAddrBook::Address](iaddrbook-address.md) übergeben werden soll, müssen das **lpfnABSDI-Element** immer auf NULL festlegen. Wenn das DIALOG_SDI-Flag festgelegt ist, legt MAPI es auf eine gültige Funktion fest, bevor es zurückgegeben wird. Clients rufen diese Funktion in ihrer Nachrichtenschleife auf, um sicherzustellen, dass Zugriffstasten im Adressbuchdialogfeld funktionieren. Wenn das Dialogfeld geschlossen wird und MAPI die Funktion aufruft, auf die der **lpfnDismiss-Member** verweist, sollten Clients die **ACCELERATEABSDI-Funktion** aus ihrer Nachrichtenschleife entfernen. 
    
**lpfnDismiss**
  
> Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL basiert. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das DIALOG_SDI-Kennzeichen angegeben. MAPI ruft die **DISMISSMODELESS-Funktion** auf, wenn der Benutzer das Dialogfeld "Adresse ohne Modus" schließt und einen Client, der **IAddrBook::Address aufruft,** informiert, dass das Dialogfeld nicht mehr aktiv ist. 
    
**lpvDismissContext**
  
> Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS-Funktion** übergeben werden sollen, auf die vom **Member "lpfnDismiss"** verwiesen wird. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festzulegende DIALOG_SDI-Kennzeichen angegeben. 
    
**lpszCaption**
  
> Zeiger auf Text, der als Titel für das allgemeine Adressdialogfeld verwendet werden soll.
    
**lpszNewEntryTitle**
  
> Zeiger auf Text, der als Schaltflächenbeschriftung für die Schaltfläche verwendet werden soll, die entweder das Dialogfeld **"Neuer Eintrag"** oder ein anderes Dialogfeld aufruft. 
    
**lpszDestWellsTitle**
  
> Zeiger auf Text, der als Titel für die Empfängertextfeld-Steuerelemente verwendet werden soll, die in der modalen Version des allgemeinen Adressdialogfelds angezeigt werden können. Dieser Member wird nicht für Dialogfelder ohne Modus verwendet. 
    
**cDestFields**
  
> Anzahl der Empfängertextfeld-Steuerelemente in der modalen Version des Adressdialogfelds oder Null, wenn das Dialogfeld moduslos ist. Das Adressdialogfeld ist nur zum Durchsuchen geöffnet, wenn die folgenden Bedingungen erfüllt sind: 
    
  - Der **cDestFields-Member** ist auf Null festgelegt. 
    
  - Das DIALOG_BOX-Kennzeichen ist festgelegt.
    
  - Das ADDRESS_ONE-Flag ist nicht festgelegt.
    
  Das Festlegen von **"cDestFields"** auf 0XFFFFFFFF impliziert, dass die MAPI die Standardanzahl der Empfängertextfeld-Steuerelemente erstellen sollte. In diesem Fall müssen die **Member lppszDestTitles** und **lpulDestComps** NULL sein. 
    
**nDestFieldFocus**
  
> Gibt das bestimmte Textfeld-Steuerelement an, das den anfänglichen Fokus haben soll, wenn die modale Version des Dialogfelds angezeigt wird. Dieser Wert muss zwischen 0 und dem Wert von **cDestFields** minus 1 sein. 
    
**lppszDestTitles**
  
> Zeiger auf ein Array von Beschriftungen für Schaltflächen, die den einzelnen Textfeld-Steuerelementen zugeordnet sind, die in der modalen Version des Adressdialogfelds angezeigt werden. Der Wert des **cDestFields-Elements** gibt die Anzahl der im Array enthaltenen Beschriftungen an. Wenn der **LppszDestTitles-Member** NULL ist, verwendet die **Address-Methode** Standardtitel. 
    
**lpulDestComps**
  
> Zeiger auf ein Array von Empfängertypwerten, z. B. MAPI_TO, MAPI_CC und MAPI_BCC, das jedem Textfeld-Steuerelement zugeordnet ist. Der Wert des **CDestFields-Elements** gibt die Anzahl der Empfängertypen an, die im Array enthalten sind. Die Werte, auf die von **lpulDestComps** verwiesen wird, können verwendet werden, um die **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft jedes Empfängers festzulegen. Wenn der **LpulDestComps-Member** NULL ist, verwendet die **Address-Methode** standardmäßige Empfängertypen. 
    
**lpContRestriction**
  
> Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die den Typ der Adresseinträge einschränkt, die im Dialogfeld angezeigt werden können. 
    
**lpHierRestriction**
  
> Zeiger auf eine **SRestriction-Struktur,** die die Adressbuchcontainer einschränkt, die Adresseinträge bereitstellen können, die im Dialogfeld angezeigt werden sollen. 
    
## <a name="remarks"></a>HinwBemerkungeneise

**ADRPARM-Strukturen** werden von Clients und Dienstanbietern verwendet, um das Aussehen und Verhalten der allgemeinen MAPI-Adressdialogfelder zu steuern. Es gibt zwei Varianten des Adressdialogfelds: moduslos und modal. Einige der Elemente in der **ADRPARM-Struktur** gelten für beide Versionen des Dialogfelds, andere nur für eine der beiden Versionen. Die folgende Tabelle verknüpft die Elemente einer **ADRPARM-Struktur** mit ihrer Verwendung mit den allgemeinen Adressdialogfeldern. 
  
|ADRPARM-Mitglied|Typ des Dialogfelds|
|:-----|:-----|
|**cbABContEntryID** und **lpABContEntryID** <br/> |Modal und moduslos  <br/> |
|**ulFlags** <br/> |Modal und moduslos  <br/> |
|**lpReserved** <br/> |Modal und moduslos  <br/> |
|**ulHelpContext** und **lpszHelpFileName** <br/> |Modal und moduslos  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss** und **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |Modal und moduslos  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** und **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal und moduslos  <br/> |
|**lpHierRestriction** <br/> |Modal und moduslos  <br/> |
   
Das Dialogfeld ohne Modus ist eine schreibgeschützte Anzeige von Einträgen aus einem oder mehreren Adressbuchcontainern. Das Dialogfeld kann alle Einträge aus den ausgewählten Containern anzeigen oder auf die Einträge und Container beschränkt sein, die den durch eine Einschränkung festgelegten Kriterien entsprechen. Die Inhaltseinschränkung, auf die von **lpContRestriction** verwiesen wird, kann die angezeigten Eintragstypen einschränken, und die Hierarchieeinschränkung, auf die von **lpHierRestriction** verwiesen wird, kann die Container einschränken, die die Einträge bereitstellen. Um den Aufrufer zu informieren, wenn das Dialogfeld geschlossen wird, ruft MAPI eine Funktion auf, die vom Aufrufer bereitgestellt wird, die dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) entspricht. Eine weitere Funktion, die dem [ACCELERATEABSDI-Prototyp](accelerateabsdi.md) entspricht, wird von der MAPI bereitgestellt und vom Aufrufer in der Windows Meldungsschleife aufgerufen, um das Arbeiten von Tastenkombinationen zu vereinfachen. Die moduslose Version des MAPI-Adressdialogfelds kann angezeigt werden, wenn Clients [IAddrBook::Address](iaddrbook-address.md) aufrufen oder wenn Dienstanbieter [IMAPISupport::Address](imapisupport-address.md)aufrufen. 
  
Das modale Dialogfeld ist eine Lese-/Schreibzugriffsanzeige von Einträgen aus einem oder mehreren Containern. Der Inhalt kann auf die gleiche Weise wie die moduslose Version durch Einschränkungen beeinflusst werden, die in den **Membern lpContRestriction** und **lpHierRestriction** festgelegt sind. Zusätzlich zum Listenfeld, in dem Containereinträge angezeigt werden, kann das modale Dialogfeld zwischen ein und drei Textfeld-Steuerelementen für das Halten der vom Benutzer ausgewählten Einträge enthalten. Jedes Bearbeitungssteuerelement ist einem bestimmten Empfängertyp oder **einer bestimmten PR_RECIPIENT_TYPE** Eigenschaft zugeordnet, z. B. MAPI_TO. Das modale Adressdialogfeld kann durch eine der **Address -Methoden** angezeigt werden oder wenn Clients [IAddrBook::D etails](iaddrbook-details.md) aufrufen und Dienstanbieter [IMAPISupport::D etails](imapisupport-details.md)aufrufen. 
  
Diese Abbildung enthält zwei Textfeld-Steuerelemente, da das **cDestFields-Element** der **ADRPARM-Struktur,** die die Anzeige dieses Dialogfelds steuert, auf 2 festgelegt ist. Das erste Steuerelement hat den anfänglichen Fokus, da das **nDestFieldFocus-Element** auf 0 festgelegt ist. 
  
Das **LpszNewEntryTitle-Element** zeigt auf Text für eine Schaltflächenbeschriftung, die bei Auswahl ein zusätzliches Dialogfeld anzeigt. In der Regel wird wie in der Abbildung des modalen Dialogfelds gezeigt, die Schaltfläche mit der Bezeichnung **"Neu"** bezeichnet, und das daraufhin angezeigte Dialogfeld listet alle Arten von Adressen auf, die von einem der Adressbuchanbieter im Profil erstellt werden können. Clients bewirken, dass dieses Dialogfeld **"Neuer Eintrag"** angezeigt wird, indem [IAddrBook::NewEntry](iaddrbook-newentry.md) aufgerufen wird und null für den  _cbEidNewEntryTpl-Parameter_ übergeben wird, und NULL für den  _LpEidNewEntryTpl-Parameter,_ wenn der Benutzer die Schaltfläche auswählt. Die Informationen, die in diesem Dialogfeld enthalten sind, stammen aus der EINMALIGEN MAPI-Tabelle. 
  
Jeder Eintrag in diesem Dialogfeld ist einer Vorlage für die Eingabe der Daten zugeordnet, die zum Erstellen einer Adresse des bestimmten Typs erforderlich sind. Die meisten Adressbuchanbieter stellen eine Vorlage für jeden Adresseintragstyp bereit, den sie erstellen können. Wenn ein Benutzer in diesem Dialogfeld eine Auswahl trifft, zeigt MAPI die entsprechende Vorlage an.
  
Die wichtigsten vier Bits des **ulFlags-Elements** der **ADRPARM-Struktur** enthalten eine Versionsnummer, die die Version der **ADRPARM-Struktur** identifiziert. Die aktuelle Version ist 0 (null) oder ADRPARM_HELP_CTX. Die aktuelle Implementierung der MAPI schlägt für eine andere Version der Struktur als Null fehl. 
  
Zukünftige Versionen der Struktur können völlig unterschiedlich sein; sie unterstützen möglicherweise die Version-Null-Struktur nicht. Die folgenden Makros werden bereitgestellt, um die Versionsnummer aus dem **ulFlags-Element** zu extrahieren und mit den definierten Flags zu kombinieren: 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Siehe auch

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [MAPI-Strukturen](mapi-structures.md)

