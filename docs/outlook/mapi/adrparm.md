---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425897"
---
# <a name="adrparm"></a>ADRPARM

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Anzeige und das Verhalten des Allgemeinen Adressdialogfelds. 
  
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

## <a name="members"></a>Elemente

**cbABContEntryID**
  
> Anzahl der Bytes in der Eintrags-ID, auf die **von lpABContEntryID verwiesen wird.**
    
**lpABContEntryID**
  
> Zeiger auf die Eintrags-ID des Containers, der die anfängliche Liste der Empfängeradressen ansent, die im Dialogfeld Adresse angezeigt werden.
    
**ulFlags**
  
> Bitmaske von Flags, die verschiedenen Adressdialogfeldoptionen zugeordnet sind. Die folgenden Kennzeichen können festgelegt werden:
    
AB_RESOLVE
  
> Aktivieren Sie, dass alle Namen nach dem Schließen des Adressdialogfelds aufgelöst werden. Wenn aus dem Namensauflösungsprozess mehrdeutige Einträge resultieren, wird der Benutzer in einem Dialogfeld zur Lösung aufgefordert. Durch Festlegen dieses Kennzeichens wird sichergestellt, dass alle von [IAddrBook::Address](iaddrbook-address.md) zurückgegebenen Namen aufgelöst werden. 
    
AB_SELECTONLY
  
> Deaktivieren Sie die Erstellung von Einmaladressen für eine Empfängerliste. Dieses Flag wird nur verwendet, wenn das Dialogfeld modal ist, wie durch das festgelegte DIALOG_MODAL angegeben wird.
    
ADDRESS_ONE
  
> Der Benutzer kann genau einen Empfänger anstelle mehrerer Empfänger aus einer Liste auswählen. Dieses Flag ist nur gültig, **wenn cDestFields** null ist und das Dialogfeld modal ist, wie durch das festgelegte DIALOG_MODAL angegeben wird. 
    
DIALOG_MODAL
  
> Bewirkt, dass die modale Version des Allgemeinen Adressdialogfelds angezeigt wird. Entweder dieses Flag oder DIALOG_SDI muss festgelegt werden. beides kann nicht festgelegt werden. 
    
DIALOG_OPTIONS
  
> Bewirkt, **dass** die Schaltfläche "Sendeoptionen" im Dialogfeld angezeigt wird. Dieses Flag wird nur verwendet, wenn das Dialogfeld modal ist, wie durch das festgelegte DIALOG_MODAL angegeben wird. 
    
DIALOG_SDI
  
> Bewirkt, dass die moduslose Version des Allgemeinen Adressdialogfelds angezeigt wird. Entweder dieses Flag oder DIALOG_MODAL muss festgelegt werden. beides kann nicht festgelegt werden. Das DIALOG_SDI wird für Nicht-Outlook-Clients ignoriert, und die modale Version des Dialogfelds wird angezeigt. Daher sollte im  _lpulUIParam-Parameter_ von [IAddrBook::Address](iaddrbook-address.md)kein Zeiger auf ein Handle erwartet werden.
    
**lpReserved**
  
> Reserviert, muss Null sein.
    
**ulHelpContext**
  
> Gibt den Kontext in der **Hilfe** an, der angezeigt wird, wenn der Benutzer im Dialogfeld Adresse auf die Schaltfläche Hilfe klickt. 
    
**lpszHelpFileName**
  
> Zeiger auf den Namen einer Hilfedatei, die dem Dialogfeld Adresse zugeordnet wird. Das **lpszHelpFileName-Element** wird zusammen mit **ulHelpContext** verwendet, um die Windows **WinHelp-Funktion** auf aufruft. 
    
**lpfnABSDI**
  
> Zeiger auf eine MAPI-Funktion basierend auf [dem ACCELERATEABSDI-Prototyp](accelerateabsdi.md) oder NULL. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird. Clients, die eine **ADRPARM-Struktur** erstellen, die [an IAddrBook::Address](iaddrbook-address.md) übergeben wird, müssen das **lpfnABSDI-Element** immer auf NULL festlegen. Wenn das DIALOG_SDI festgelegt ist, wird mapI vor der Rückgabe auf eine gültige Funktion festgelegt. Clients rufen diese Funktion in ihrer Nachrichtenschleife auf, um sicherzustellen, dass Zugriffstasten im Adressbuchdialogfeld funktionieren. Wenn das Dialogfeld verworfen wird und MAPI die Funktion aufruft, auf die das **lpfnDismiss-Mitglied** verweist, sollten Clients denHook der **ACCELERATEABSDI-Funktion** aus ihrer Nachrichtenschleife entfließen. 
    
**lpfnDismiss**
  
> Zeiger auf eine Funktion, die auf dem [DISMISSMODELESS-Prototyp](dismissmodeless.md) oder NULL basiert. Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird. MAPI ruft die **FUNKTION DISMISSMODELESS** auf, wenn der Benutzer das Dialogfeld "Modeless Address" schließt und einen Client informiert, der **IAddrBook::Address** aufruft, dass das Dialogfeld nicht mehr aktiv ist. 
    
**lpvDismissContext**
  
> Zeiger auf Kontextinformationen, die an die **DISMISSMODELESS-Funktion** übergeben werden sollen, auf die das **lpfnDismiss-Element verweist.** Dieses Element gilt nur für die moduslose Version des Dialogfelds, wie durch das festgelegte DIALOG_SDI angegeben wird. 
    
**lpszCaption**
  
> Zeiger auf Text, der als Titel für das Dialogfeld allgemeine Adresse verwendet werden soll.
    
**lpszNewEntryTitle**
  
> Zeiger auf Text, der als Schaltflächenbeschriftung für die Schaltfläche verwendet werden soll, die entweder das Dialogfeld Neuer **Eintrag** oder ein anderes Dialogfeld aufruft. 
    
**lpszDestWellsTitle**
  
> Zeiger auf Text, der als Titel für die Steuerelemente des Empfängertextfelds verwendet werden soll, die in der modalen Version des Dialogfelds allgemeine Adresse angezeigt werden können. Dieses Element wird nicht für moduslose Dialogfelder verwendet. 
    
**cDestFields**
  
> Anzahl der Empfängertextfeldsteuerelemente in der modalen Version des Adressdialogfelds oder Null, wenn das Dialogfeld modeless ist. Das Dialogfeld Adresse ist nur geöffnet, wenn die folgenden Bedingungen erfüllt sind: 
    
  - Das **cDestFields-Element** ist auf Null festgelegt. 
    
  - Das DIALOG_BOX ist festgelegt.
    
  - Das ADDRESS_ONE ist nicht festgelegt.
    
  Das Festlegen von **cDestFields** auf 0XFFFFFFFF bedeutet, dass MAPI die Standardanzahl von Empfängertextfeldsteuerelementen erstellen sollte. In diesem Fall müssen **die Elemente lppszDestTitles** und **lpulDestComps** NULL sein. 
    
**nDestFieldFocus**
  
> Gibt das bestimmte Textfeldsteuerelement an, das den anfänglichen Fokus haben sollte, wenn die modale Version des Dialogfelds angezeigt wird. Dieser Wert muss zwischen 0 und dem Wert von **cDestFields** minus 1 liegen. 
    
**lppszDestTitles**
  
> Zeiger auf ein Array von Beschriftungen für Schaltflächen, die den einzelnen Textfeldsteuerelementen zugeordnet sind, die in der modalen Version des Adressdialogfelds angezeigt werden. Der Wert des **cDestFields-Members** gibt die Anzahl der Bezeichnungen an, die im Array enthalten sind. Wenn das **lppszDestTitles-Element** NULL ist, verwendet die **Address-Methode** Standardtitel. 
    
**lpulDestComps**
  
> Zeiger auf ein Array von Empfängertypwerten, z. B. MAPI_TO, MAPI_CC und MAPI_BCC, das jedem Textfeldsteuerelement zugeordnet ist. Der Wert des **CDestFields-Mitglieds** gibt die Anzahl der Empfängertypen an, die im Array enthalten sind. Die von **lpulDestComps** angegebenen Werte können zum Festlegen der **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) -Eigenschaft jedes Empfängers verwendet werden. Wenn das **lpulDestComps-Element** NULL ist, verwendet die **Address-Methode** Standardempfängertypen. 
    
**lpContRestriction**
  
> Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die den Typ der Adresseinträge einschränkt, die im Dialogfeld angezeigt werden können. 
    
**lpHierRestriction**
  
> Zeiger auf eine **SRestriction-Struktur,** die die Adressbuchcontainer einschränkt, die Adresseinträge angeben können, die im Dialogfeld angezeigt werden können. 
    
## <a name="remarks"></a>Hinweise

**ADRPARM-Strukturen** werden von Clients und Dienstanbietern verwendet, um die Darstellung und das Verhalten der Dialogfelder für allgemeine MAPI-Adressen zu steuern. Es gibt zwei Varianten des Adressdialogfelds: modeless und modal. Einige Elemente in der **ADRPARM-Struktur** gelten für beide Versionen des Dialogfelds, einige jedoch nur für eine der beiden Versionen. In der folgenden Tabelle werden die Elemente einer **ADRPARM-Struktur** mit ihrer Verwendung mit den allgemeinen Adressdialogfeldern in Beziehung setzen. 
  
|ADRPARM-Mitglied|Typ des Dialogfelds|
|:-----|:-----|
|**cbABContEntryID** und **lpABContEntryID** <br/> |Modal und modeless  <br/> |
|**ulFlags** <br/> |Modal und modeless  <br/> |
|**lpReserved** <br/> |Modal und modeless  <br/> |
|**ulHelpContext** und **lpszHelpFileName** <br/> |Modal und modeless  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss** und **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |Modal und modeless  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles** und **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modal und modeless  <br/> |
|**lpHierRestriction** <br/> |Modal und modeless  <br/> |
   
Das Dialogfeld ohne Modus ist eine schreibgeschützte Anzeige von Einträgen aus einem oder mehreren Adressbuchcontainern. Das Dialogfeld kann alle Einträge aus den ausgewählten Containern anzeigen oder auf die Einträge und Container beschränkt sein, die den durch eine Einschränkung festgelegten Kriterien entsprechen. Die inhaltseinschränkung, auf die **von lpContRestriction** verwiesen wird, kann die Angezeigten Typen von Einträgen einschränken, und die Hierarchieeinschränkung, auf die **durch lpHierRestriction** verwiesen wird, kann die Container einschränken, die die Einträge bereitstellen. Um den Anrufer zu informieren, wenn das Dialogfeld gesperrt wird, ruft MAPI eine Funktion auf, die vom Aufrufer bereitgestellt wird, die dem [PROTOTYP VON DISMISSMODELESS](dismissmodeless.md) entspricht. Eine weitere Funktion, die dem [ACCELERATEABSDI-Prototyp](accelerateabsdi.md) entspricht, wird von MAPI bereitgestellt und vom Anrufer in der Windows-Nachrichtenschleife aufgerufen, um das Arbeiten von Tastenkombinationen zu erleichtern. Die moduslose Version des Dialogfelds MAPI-Adresse kann angezeigt werden, wenn Clients [IAddrBook::Address](iaddrbook-address.md) aufrufen oder wenn Dienstanbieter [IMAPISupport::Address aufrufen.](imapisupport-address.md) 
  
Das modale Dialogfeld ist eine Lese-/Schreibanzeige von Einträgen aus einem oder mehreren Containern. Der Inhalt kann auf die gleiche Weise wie die moduslose Version durch Einschränkungen beeinflusst werden, die in den **Mitgliedern lpContRestriction** und **lpHierRestriction festgelegt** sind. Zusätzlich zum Listenfeld, in dem Containereinträge angezeigt werden, kann das modale Dialogfeld zwischen einem und drei Textfeldsteuerelementen zum Halten von vom Benutzer ausgewählten Einträgen enthalten. Jedes Bearbeitungssteuerelement ist einem bestimmten Empfängertyp oder einer bestimmten **PR_RECIPIENT_TYPE** zugeordnet, z. B. MAPI_TO. Das Dialogfeld modale Adresse kann von einer der **Address-Methoden** angezeigt werden oder wenn Clients [IAddrBook::D etails](iaddrbook-details.md) aufrufen und Dienstanbieter [IMAPISupport::D etails](imapisupport-details.md)aufrufen. 
  
Diese Abbildung enthält zwei Textfeldsteuerelemente, da **das cDestFields-Element** der **ADRPARM-Struktur,** die die Anzeige dieses Dialogfelds steuert, auf 2 festgelegt ist. Das erste Steuerelement hat den anfänglichen Fokus, da **das Element nDestFieldFocus** auf 0 festgelegt ist. 
  
Das **lpszNewEntryTitle-Element** zeigt auf Text für eine Schaltflächenbeschriftung, die bei Auswahl ein zusätzliches Dialogfeld angezeigt wird. Wie in der Abbildung des modalen Dialogfelds gezeigt, wird die Schaltfläche in der Regel als **Neu** gekennzeichnet, und das angezeigte Dialogfeld listet alle Typen von Adressen auf, die von einem der Adressbuchanbieter im Profil erstellt werden können. Clients führen  dazu, dass dieses Dialogfeld Neuer Eintrag angezeigt wird, indem [IAddrBook::NewEntry](iaddrbook-newentry.md) und null für den _cbEidNewEntryTpl-Parameter_ und NULL für den _lpEidNewEntryTpl-Parameter_ zurückgegeben werden, wenn der Benutzer die Schaltfläche auswählt. Die Informationen, die in diesem Dialogfeld enthalten sind, stammen aus der einmal aufgeführten MAPI-Tabelle. 
  
Jeder Eintrag in diesem Dialogfeld ist einer Vorlage für die Eingabe der daten zugeordnet, die zum Erstellen einer Adresse des jeweiligen Typs erforderlich sind. Die meisten Adressbuchanbieter bieten eine Vorlage für jeden Adresseintrag, den sie erstellen können. Wenn ein Benutzer eine Auswahl aus diesem Dialogfeld vor nimmt, zeigt MAPI die entsprechende Vorlage an.
  
Die wichtigsten vier Bits des **ulFlags-Mitglieds** der **ADRPARM-Struktur** enthalten eine Versionsnummer, die die Version der **ADRPARM-Struktur** identifiziert. Die aktuelle Version ist 0 (Null) oder ADRPARM_HELP_CTX. Bei der aktuellen Implementierung von MAPI wird für jede andere Version der Struktur als Null ein Fehler angezeigt. 
  
Zukünftige Versionen der Struktur können völlig unterschiedlich sein. Die Version-Null-Struktur wird möglicherweise nicht unterstützt. Die folgenden Makros werden zum Extrahieren der Versionsnummer aus dem **ulFlags-Element** und zum Kombinieren mit den definierten Flags bereitgestellt: 
  
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

