---
title: Buchhalterumgebungen in Business Central
description: 'Erhalten Sie Informationen über das Buchhalter-Rollencenter und den Unternehmens-Hub, der interne und externe Buchhalter im Client-Unternehmen unterstützt.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: '100, 1156, 1157, 1314, 1315, 1316, 9027'
ms.date: 06/12/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="accountant-experiences-in-"></a>Buchhalterumgebungen in [!INCLUDE[prod_long](includes/prod_long.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Jedes Unternehmens muss seine Bücher führen und die Buchhaltung genehmigen. Einige Unternehmen verwenden einen externen Buchhalter, und andere haben einen Buchhalter als Mitarbeiter. Unabhängig von der Art Buchhalter, der Sie sind, können Sie das **Buchhalter**-Rollencenter als Home-Bildschirm in [!INCLUDE[prod_short](includes/prod_short.md)] verwenden. Von hier können Sie auf alle Seiten zugreifen, die Sie in Ihrer Arbeit benötigen.  

## <a name="accountant-role-center"></a>Buchhalter-Rollencenter

Das Rollencenter bildet ein Dashboard mit Aktivitätskacheln, die Ihnen Echtzeitkennzahlen anzeigen und Ihnen Zugriff auf die Daten geben. Das Menüband oben auf der Seite bietet Ihnen Zugriff auf weitere Aktionen. Beispielsweise zum Öffnen von Finanzberichten und Kontoauszügen in Excel. Im Navigationsbereich links können Sie schnell zwischen den Listen wechseln, die Sie häufig verwenden. Hier finden Sie weitere Regionen, wie etwa **Gebuchte Belege** mit den verschiedenen Belegarten, die der Mandant gebucht hat.  

Wenn Sie neu sind bei [!INCLUDE[prod_short](includes/prod_short.md)] können Sie eine Liste der Videos starten direkt von Ihrem Rollencenter aus. Sie können auch **Erste Schritte** starten, die die Schlüsselbereiche unterstreichen.  

## <a name="company-hub"></a>Unternehmens-Hub

Wenn Sie in mehreren [!INCLUDE [prod_short](includes/prod_short.md)]-Unternehmen arbeiten, könnte es nützlich sein, die Seite **Unternehmens-Hub** zu verwenden, um den Überblick über die Arbeit zu behalten. Weitere Informationen finden Sie unter [Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten](company-hub.md).  

## <a name="inviting-your-external-accountant-to-your-"></a><a name="inviteaccountant"></a>Ihren externen Buchhalter einladen zu Ihrem [!INCLUDE[prod_short](includes/prod_short.md)]

Wenn Sie einen externen Buchhalter verwenden, um Ihre Bücher und Finanzberichterstattung zu verwalten, kann Ihr Administrator sie für Ihr [!INCLUDE[prod_short](includes/prod_short.md)] einladen, damit sie mit Ihnen an Ihren steuerlichen Daten arbeiten. [!INCLUDE[prod_short](includes/prod_short.md)] enthält drei Lizenzen des Typs „Externer Buchhalter“. Weitere Informationen über die Lizenzierung können Sie unter [Microsoft Dynamics 365 Business Central Lizenzleitfaden](https://go.microsoft.com/fwlink/?LinkId=866544) herunterladen.

Sobald Ihr Buchhalter Zugriff auf [!INCLUDE[prod_short](includes/prod_short.md)] hat, können sie das Rollencenter **Buchhalter** für einen einfachen Zugriff auf die Seiten für ihre Arbeit verwenden. Sie können den Unternehmens-Hub auch in ihrem eigenen [!INCLUDE [prod_short](includes/prod_short.md)] nutzen, um ihre Arbeit zu verwalten. Weitere Informationen finden Sie unter [Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten](company-hub.md).  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4Fnyw?rel=0]

Es ist einfach, Ihren externen Buchhalter einzuladen. Öffnen Sie die Seite **Benutzer** und wählen Sie im Band die Aktion **Externen Buchhalter einladen**. Es wird eine E-Mail für Sie vorbereitet. Sie tragen einfach nur die E-Mail-Adresse Ihres Buchhalters ein und senden die Einladung ab.  

> [!Note]  
> Dies setzt voraus, dass Sie SMPT-E-Mail eingerichtet haben. Weitere Informationen finden Sie unter [E-Mail einrichten](admin-how-setup-email.md).  

<!-- ![Invite your accountant.](./media/finance-invite-accountant/invite-accountant.png)-->

> [!IMPORTANT]  
> Die E-Mail-Adresse des Buchhalters muss eine Arbeitsadresse sein, die auf Microsoft Entra-ID basiert. Wenn der Buchhalter eine andere Art von E-Mail verwendet, kann die Einladung nicht gesendet werden.
>
> Diese Aufgabe erfordert den Zugriff auf die Verwaltung von Benutzern und Lizenzen in Microsoft Entra-ID. Dem Benutzer, der diese Einladung sendet, muss mindestens die Rolle  [Benutzeradministrator](/entra/identity/role-based-access-control/permissions-reference#user-administrator)  in  Microsoft 365 Admin Center zugewiesen sein. Weitere Informationen finden Sie unter [Informationen zu Administratorrollen](/microsoft-365/admin/add-users/about-admin-roles) im Microsoft 365-Administratorinhalt.  

### <a name="add-your-accountant-to-your-microsoft-365-in-the-azure-portal"></a>Ihren Buchhalter zu Microsoft 365 im Azure-Portal hinzufügen

Wenn Ihr Administrator oder Wiederverkäufer die Anleitung **Externen Buchhalter einladen** nicht verwenden möchten, können sie im Azure-Portal einen externen Benutzer hinzufügen und diesem Benutzer die Lizenz *Externer Buchhalter* zuweisen. Weitere Informationen finden Sie unter [Schnellstart: Ihrem Verzeichnis im Azure-Portal Gastbenutzer hinzufügen](/azure/active-directory/b2b/b2b-quickstart-add-guest-users-portal).

#### <a name="to-add-your-accountant-as-a-guest-user"></a>So fügen Sie Ihren Buchhalter als Gastbenutzer hinzu

1. Öffne Sie das [Azure-Portal](https://portal.azure.com/).
2. Wählen Sie im linken Bereich **Microsoft Entra ID**.
3. Unter **Verwalten** wählen Sie **Benutzer**.
4. Wählen Sie **Neuer Gastbenutzer**.
5. Wählen Sie auf der Seite **Neuer Benutzer** die Option **Benutzer einladen** aus und fügen Sie Ihrem externen Buchhalter dann Informationen hinzu.  

   Schliessen Sie optional eine persönliche Begrüssungsnachricht an den Buchhalter ein, um ihn darüber zu informieren, dass Sie ihn Ihrem [!INCLUDE[prod_short](includes/prod_short.md)] hinzufügen.

6. Wählen Sie **Einladen**, um die Einladung automatisch zu versenden. Oben rechts wird eine Benachrichtigung mit der Meldung **Erfolgreich eingeladener Benutzer** angezeigt. 
7. Nachdem Sie die Einladung gesendet haben, wird das Benutzerkonto automatisch als Gast zum Verzeichnis hinzugefügt.

Als Nächstes müssen Sie dem neuen Gastbenutzer eine Lizenz für [!INCLUDE[prod_short](includes/prod_short.md)] zuweisen.

#### <a name="to-give-your-accountant-access-to-your-"></a>So geben Sie Ihrem Buchhalter Zugriff auf Ihre [!INCLUDE[prod_short](includes/prod_short.md)]

1. Wählen Sie im Azure-Portal für den neu hinzugefügten Benutzer **Profil** und dann Sie **Bearbeiten** aus
2. Aktualisieren Sie die Feld **Verbrauchsort** auf das entsprechende Land bzw. die entsprechende Region, und wählen Sie dann **Speichern** aus.
3. Wählen Sie **Lizenzen** und öffnen Sie dann **Zuordnungen**.
4. Wählen Sie die Lizenz **Externer Dynamics 365 Business Central-Buchhalter**.  
    
    Wenn diese Lizenz nicht verfügbar ist, wenden Sie sich an Ihren Wiederverkaufspartner, um die Lizenz Ihrem Abonnement hinzuzufügen.

    Speziell für Evaluierungszwecke in einem Testtenant können Sie stattdessen eine **Dynamics 365 Business Central für IWs** Lizenz verwenden. Sie können diese Art von Lizenz jedoch nicht verwenden, wenn Sie [!INCLUDE[prod_short](includes/prod_short.md)] bereits gekauft haben. 
5. Speichern Sie die Zuordnung.

Bei Erfolg wird dem Gastbenutzer die Lizenz zugewiesen und das Gastkonto wird erstellt.

### <a name="import-the-new-user-into-"></a>Den neuen Benutzer in [!INCLUDE[prod_short](includes/prod_short.md)] importieren

Der Buchhalter erhält eine E-Mail, in der er darüber informiert wird, dass er Zugriff auf Ihr Microsoft Entra-ID erhalten hat. Als Nächstes müssen Sie ihnen Zugriff auf das richtige Unternehmen in [!INCLUDE[prod_short](includes/prod_short.md)] gewähren.

#### <a name="to-add-the-accountant-to-the-right-company"></a>Hinzufügen des Buchhalters zum richtigen Unternehmen

1. Öffnen Sie das [!INCLUDE[prod_short](includes/prod_short.md)]-Unternehmen, auf die Sie dem Buchhalter Zugriff gewähren möchten unter [https://businesscentral.dynamics.com](https://businesscentral.dynamics.com).
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Benutzer** ein, und wählen Sie dann den entsprechenden Link.  
3. Wählen Sie die Aktion **Neue Benutzer von Microsoft 365 abrufen** aus.

Diese Aktion importiert das Benutzerkonto, das Sie im Azure-Portal erstellt haben, in das Unternehmen. Weitere Informationen finden Sie unter [Hinzufügen eines Benutzers in Business Central](ui-how-users-permissions.md#adduser).  

Wenn Sie mehreren Unternehmen Zugriff gewähren möchten, müssen Sie sich bei jedem Unternehmen anmelden und diesen Vorgang wiederholen. Alternativ können Sie die Berechtigungsgruppen für das Benutzerprofil des Buchhalters in [!INCLUDE[prod_short](includes/prod_short.md)] aktualisieren, wie das Zuweisen der *D365 Bus Premium*-Benutzergruppe. Weitere Informationen finden Sie unter [Berechtigungen für Benutzer und Gruppen zuweisen](ui-define-granular-permissions.md).  

## <a name="see-also"></a>Siehe auch

[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md)  
[Beenden von Jahresabschluss und Perioden](year-close-years-periods.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Finanzauswertungen in Excel analysieren](finance-analyze-excel.md)  
[Arbeit über mehrere Unternehmen hinweg im Unternehmens-Hub verwalten](company-hub.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Einrichten der Cashflowanalyse](finance-setup-cash-flow-analyses.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
