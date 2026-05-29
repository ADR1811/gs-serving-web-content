.PHONY: dev run watch test build clean

# Hot-reload dans UN seul terminal : recompilation continue + appli, en parallèle.
# Ctrl+C coupe les deux proprement (trap 'kill 0' tue tout le groupe de process).
dev:
	@trap 'kill 0' EXIT INT TERM; \
		./gradlew classes -t & \
		./gradlew bootRun; \
		wait

# Lance l'application Spring Boot (sans hot-reload)
run:
	./gradlew bootRun

# Recompile en continu dès qu'un fichier source change (à lancer dans un 2e terminal)
# Couplé à DevTools, ça donne le hot-reload : sauvegarde -> recompile -> redémarrage auto
watch:
	./gradlew classes -t

# Lance les tests
test:
	./gradlew test

# Compile le projet
build:
	./gradlew build

# Nettoie les artefacts de build
clean:
	./gradlew clean
