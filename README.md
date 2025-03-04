define make-deprecated-target
$1:
	@echo
	@printf %s\\n '$(call banner-style,Deprecated make call: make $1 $(JUSTFLAGS))'
	@printf %s\\n '$(call banner-style,Consider using just instead: just $(JUSTFLAGS) $1)'
	@echo
	just $(JUSTFLAGS) $1
endef
